#### Exercices
1. Search all sequences containing "Loxondota" in ``/home/student/lorem.txt``
    > Flag : BC{GREP_ME_LOREM_FL4G}
1. Copy the file /etc/passwd to your home directory. Display the line starting with ``student`` name.
    > Your commands :
    cp /etc/passwd /home/student/
    grep -rn passwd -e "student"
1. Display the lines in the passwd file starting with login names of 3 or 4 characters.
    > Your commands : awk -F: '{if(length($1) == 3 || (length($1) == 4)) print $1}' passwd
1. In the file ``/home/student/sample.txt`` how many different values are there in the first column? in the second?
    > Your response : 4 in each column.
    > Your command :cut -d "," -f 1 /home/student/sample.txt | sort -u | wc -l
1. In the file ``/home/student/sample.txt`` sort the values in the second column by frequency of occurrence. (uniq -c can be useful)
    > Your command : cut -d "," -f 2 /home/student/sample.txt | sort | uniq -c | sort
1. In the file ``/home/student/iris.data`` Change the column separator (comma) to tab (make sure that the changes are applied to the file)
    > Your command : sed 's/,/\t/g' iris.data > iris.data.parsed
1. In the file ``/home/student/iris.data``, extract from this file the column 3 (petal length in cm) (use cut )
    > Your command : cut -f3 d$'\t' iris.data.parsed
1. In the file ``/home/student/iris.data``, count the number of flower species (cut and uniq)
    > Your response : 3
    > Your command : cut -f5 d$'\t' iris.data.parsed | uniq
1. In the file ``/home/student/iris.data``, sort by increasing petal length (see sort options)
    > Your command : sort -k 3 iris.data.parsed
1. In the file ``/home/student/iris.data``, show only lines with petal length greater than the average size
    > Your command : average=`awk '{ total += $3 } END {print total/NR}' /home/student/iris.data`
1. Using ``/etc/passwd``, extract the user and home directory fields for all users on your student
machine for which the shell is set to ``/bin/false``. 
    > Your command : grep "/bin/false$" /etc/passwd | cut -d ":" -f 1,6
