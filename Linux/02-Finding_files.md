#### Exercises 
1. Create a file named ``my-file.txt`` with the touch command. Then execute the ``locate my-file.txt`` command. Do you find the file? 
    > Your response : no
1. Run the command sudo ``updatedb``. And run the locate my-file.txt command again. Do you find your file ?
    > Your response : yes
1. With the command ``which``, find the executable file nc and indicate the path
    > Path : /bin/nc
1. With the command ``which``, find the executable file becode. What is the flag ?
    > Command : which becode
    > Flag : BC{WH1CH_FL4G_EXECUTLE_FILE}
1. Search with ``find ``command for a file that contains the name "Edgar Allan Poe". What is the flag ?
    > Command :
    > Flag : BC{3d54r_4ll4n_P03_FL45}
1. Using the ``find`` command, find the file password.txt and specify the flag.
    > Command : find / -name "password.txt" 2>&-
    > Flag : BC{PASSWORD_FILE}
1. With the command ``find``, find a file that starts with ``becode-`` and ends with ``.sh``.
    > Command : find / -name "becode-*" 2>&-
    > Flag : BC{FLAG_FIND_PARTIAL_PATH}
1. Using the ``find`` command to identify any file (not directory) modified in the last day, NOT owned by the root
user and execute ls -l on them. **Chaining/piping commands is NOT allowed!**
    > Your command : find / -type f -mtime -1 -print ! -user root
1. With the find command, find all the files that have an authorization of ``0777``.
    > Your command : find / -type f -perm 0777
1. With the find command, find all the files in the folder ``/home/student/findme/`` that have an authorization of ``0777`` and change the rights of these files to ``0755``
    > Your command : find /home/student/findme/ -type f -perm 0777 -exec chmod 0755 {} \;
