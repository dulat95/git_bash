# Работа с git и bash  

Veronika@LAPTOP-BJACTRKT MINGW64 ~/bash1.txt
$ cd ~

Veronika@LAPTOP-BJACTRKT MINGW64 ~
$ basename "$PWD"
Veronika

Veronika@LAPTOP-BJACTRKT MINGW64 ~
$ mkdir test1

Veronika@LAPTOP-BJACTRKT MINGW64 ~
$ cd test1

Veronika@LAPTOP-BJACTRKT MINGW64 ~/test1
$ touch 1 2 3

Veronika@LAPTOP-BJACTRKT MINGW64 ~/test1
$ ls
1  2  3

Veronika@LAPTOP-BJACTRKT MINGW64 ~/test1
$ cd ~

Veronika@LAPTOP-BJACTRKT MINGW64 ~
$ mkdir test2

Veronika@LAPTOP-BJACTRKT MINGW64 ~
$ rmdir test2

Veronika@LAPTOP-BJACTRKT MINGW64 ~
$ rm ~/test1/2

Veronika@LAPTOP-BJACTRKT MINGW64 ~
$ mkdir test3 touch ~/test3/file1 ~/test3/file2

Veronika@LAPTOP-BJACTRKT MINGW64 ~
$ rm -r test3

Veronika@LAPTOP-BJACTRKT MINGW64 ~
$ mkdir test4

Veronika@LAPTOP-BJACTRKT MINGW64 ~
$ mv ~/test1/1 ~/test1/3 ~/test4/

Veronika@LAPTOP-BJACTRKT MINGW64 ~
$ echo -e "line\nline\nline" >> ~/test4/1

Veronika@LAPTOP-BJACTRKT MINGW64 ~
$ cat ~/test4/1
line
line
line

Veronika@LAPTOP-BJACTRKT MINGW64 ~
$ echo -e "line\nline\nline" >> ~/test4/3

Veronika@LAPTOP-BJACTRKT MINGW64 ~
$ cat ~/test4/1 ~/test4/3
line
line
line
line
line
line

Veronika@LAPTOP-BJACTRKT MINGW64 ~
$ nano ~/test4/1

Veronika@LAPTOP-BJACTRKT MINGW64 ~
$ cd ~
echo "cd ~" >> bash2.txt

Veronika@LAPTOP-BJACTRKT MINGW64 ~
$ mkdir test3
echo "mkdir test3" >> bash2.txt

Veronika@LAPTOP-BJACTRKT MINGW64 ~
$ echo -e "row1\nrow2\nrow3\nrow4" > ~/test3/4
echo -e "row1\nrow2\nrow3\nrow4" > ~/test3/5
echo -e "row1\nrow2\nrow3\nrow4" > ~/test3/6
echo "echo -e 'row1\nrow2\nrow3\nrow4' > ~/test3/4" >> bash2.txt
echo "echo -e 'row1\nrow2\nrow3\nrow4' > ~/test3/5" >> bash2.txt
echo "echo -e 'row1\nrow2\nrow3\nrow4' > ~/test3/6" >> bash2.txt

Veronika@LAPTOP-BJACTRKT MINGW64 ~
$ grep "row2" ~/test3/5
echo "grep 'row2' ~/test3/5" >> bash2.txt
row2

Veronika@LAPTOP-BJACTRKT MINGW64 ~
$ grep "row" ~/test3/*
echo "grep 'row' ~/test3/*" >> bash2.txt
/c/Users/Veronika/test3/4:row1
/c/Users/Veronika/test3/4:row2
/c/Users/Veronika/test3/4:row3
/c/Users/Veronika/test3/4:row4
/c/Users/Veronika/test3/5:row1
/c/Users/Veronika/test3/5:row2
/c/Users/Veronika/test3/5:row3
/c/Users/Veronika/test3/5:row4
/c/Users/Veronika/test3/6:row1
/c/Users/Veronika/test3/6:row2
/c/Users/Veronika/test3/6:row3
/c/Users/Veronika/test3/6:row4

Veronika@LAPTOP-BJACTRKT MINGW64 ~
$ grep -c "row" ~/test3/6
echo "grep -c 'row' ~/test3/6" >> bash2.txt
4

Veronika@LAPTOP-BJACTRKT MINGW64 ~
$ find ~/test3 -name "5"
echo "find ~/test3 -name '5'" >> bash2.txt
/c/Users/Veronika/test3/5

Veronika@LAPTOP-BJACTRKT MINGW64 ~
$ find ~/test3 -name "5" -exec rm {} \;
echo "find ~/test3 -name '5' -exec rm {} \;" >> bash2.txt

Veronika@LAPTOP-BJACTRKT MINGW64 ~
$ echo "test" >> ~/test3/4
echo "echo 'test' >> ~/test3/4" >> bash2.txt

Veronika@LAPTOP-BJACTRKT MINGW64 ~
$ sed -i 's/test/fail/g' ~/test3/4
echo "sed -i 's/test/fail/g' ~/test3/4" >> bash2.txt

Veronika@LAPTOP-BJACTRKT MINGW64 ~
$ echo "test" >> ~/test3/4
echo "echo 'test' >> ~/test3/4" >> bash2.txt

Veronika@LAPTOP-BJACTRKT MINGW64 ~
$ ps aux
echo "ps aux" >> bash2.txt
      PID    PPID    PGID     WINPID   TTY         UID    STIME COMMAND
     2341    1958    2341      13772  cons0     197609 13:44:54 /usr/bin/ps
     1958       1    1958      17952  cons0     197609 13:17:02 /usr/bin/bash

Veronika@LAPTOP-BJACTRKT MINGW64 ~
$ kill 666
echo "kill 666" >> bash2.txt
bash: kill: (666) - No such process

Veronika@LAPTOP-BJACTRKT MINGW64 ~
$ ping rusau.net
echo "ping rusau.net" >> bash2.txt

Обмен пакетами с rusau.net [5.181.161.75] с 32 байтами данных:
Ответ от 5.181.161.75: число байт=32 время=40мс TTL=53
Ответ от 5.181.161.75: число байт=32 время=40мс TTL=53
Ответ от 5.181.161.75: число байт=32 время=74мс TTL=56
Ответ от 5.181.161.75: число байт=32 время=46мс TTL=53

Статистика Ping для 5.181.161.75:
    Пакетов: отправлено = 4, получено = 4, потеряно = 0
    (0% потерь)
Приблизительное время приема-передачи в мс:
    Минимальное = 40мсек, Максимальное = 74 мсек, Среднее = 50 мсек

Veronika@LAPTOP-BJACTRKT MINGW64 ~
$ ping -c 5 rusau.net
echo "ping -c 5 rusau.net" >> bash2.txt
Доступ запрещен. Для параметра -c требуются права администратора.

Veronika@LAPTOP-BJACTRKT MINGW64 ~
$ curl -X GET "https://petstore.swagger.io/v2/pet/findByStatus?status=available" -H "accept: application/json"
echo "curl -X GET 'https://petstore.swagger.io/v2/pet/findByStatus?status=available' -H 'accept: application/json'" >> bash2.txt
[{"id":9223372036854762298,"category":{"id":0,"name":"string"},"name":"doggie","photoUrls":["string"],"tags":[{"id":0,"name":"string"}],"status":"available"},{"id":20,"category":{"id":0,"name":"string"},"name":"doggie","photoUrls":["string"],"tags":[{"id":0,"name":"string"}],"status":"available"},{"id":23,"category":{"id":0,"name":"string"},"name":"doggie","photoUrls":["string"],"tags":[{"id":0,"name":"string"}],"status":"available"},{"id":9223372036854762306,"category":{"id":0,"name":"string"},"name":"fish","photoUrls":["string"],"tags":[{"id":0,"name":"string"}],"status":"available"},{"id":9223372036854762307,"category":{"id":0,"name":"string"},"name":"doggie","photoUrls":["string"],"tags":[{"id":0,"name":"string"}],"status":"available"},{"id":9223372036854762319,"category":{"id":0,"name":"string"},"name":"doggie","photoUrls":["string"],"tags":[{"id":0,"name":"string"}],"status":"available"},{"id":9223372036854762321,"category":{"id":0,"name":"string"},"name":"doggie","photoUrls":["string"],"tags":[{"id":0,"name":"string"}],"status":"available"},{"id":9223372036854762324,"category":{"id":0,"name":"string"},"name":"fish","photoUrls":["string"],"tags":[{"id":0,"name":"string"}],"status":"available"},{"id":9223372036854762325,"category":{"id":0,"name":"string"},"name":"morce","photoUrls":["string"],"tags":[{"id":0,"name":"string"}],"status":"available"},{"id":9223372036854762350,"category":{"id":0,"name":"string"},"name":"doggie","photoUrls":["string"],"tags":[{"id":0,"name":"string"}],"status":"available"},{"id":9223372036854762355,"category":{"id":0,"name":"string"},"name":"Puff","photoUrls":["string"],"tags":[{"id":0,"name":"string"}],"status":"available"},{"id":9223372036854762356,"category":{"id":0,"name":"string"},"name":"doggie","photoUrls":["string"],"tags":[{"id":0,"name":"string"}],"status":"available"},{"id":9223372036854762359,"category":{"id":0,"name":"string"},"name":"doggie","photoUrls":["string"],"tags":[{"id":0,"name":"string"}],"status":"available"},{"id":9223372036854762370,"category":{"id":0,"name":"string"},"name":"fish","photoUrls":["string"],"tags":[{"id":0,"name":"string"}],"status":"available"},{"id":9223372036854762372,"category":{"id":0,"name":"string"},"name":"fish","photoUrls":["string"],"tags":[{"id":0,"name":"string"}],"status":"available"},{"id":9223372036854762373,"category":{"id":0,"name":"string"},"name":"fish","photoUrls":["string"],"tags":[{"id":0,"name":"string"}],"status":"available"},{"id":9223372036854762439,"category":{"id":0,"name":"string"},"name":"doggie","photoUrls":["string"],"tags":[{"id":0,"name":"string"}],"status":"available"},{"id":9223372036854762443,"category":{"id":0,"name":"string"},"name":"Puff","photoUrls":["string"],"tags":[{"id":0,"name":"string"}],"status":"available"},{"id":9223372036854762451,"category":{"id":0,"name":"string"},"name":"doggie","photoUrls":["string"],"tags":[{"id":0,"name":"string"}],"status":"available"},{"id":9223372036854762452,"category":{"id":0,"name":"string"},"name":"fish","photoUrls":["string"],"tags":[{"id":0,"name":"string"}],"status":"available"},{"id":9223372036854762493,"category":{"id":0,"name":"string"},"name":"doggie","photoUrls":["string"],"tags":[{"id":0,"name":"string"}],"status":"available"},{"id":9223372036854762496,"category":{"id":0,"name":"string"},"name":"doggie","photoUrls":["string"],"tags":[{"id":0,"name":"string"}],"status":"available"},{"id":9223372036854762508,"category":{"id":0,"name":"string"},"name":"doggie","photoUrls":["string"],"tags":[{"id":0,"name":"string"}],"status":"available"},{"id":9223372036854762511,"category":{"id":0,"name":"string"},"name":"fish","photoUrls":["string"],"tags":[{"id":0,"name":"string"}],"status":"available"},{"id":9223372036854762514,"name":"Doggie","photoUrls":["http://example.com/photo.jpg"],"status":"available"},{"id":9223372036854762515,"category":{"id":0,"name":"string"},"name":"doggie","photoUrls":["string"],"tags":[{"id":0,"name":"string"}],"status":"available"},{"id":9223372036854762516,"name":"AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA","photoUrls":["http://example.com/photo.jpg"],"status":"available"},{"id":9223372036854762517,"name":"Doggie","photoUrls":["http://example.com/photo.jpg"],"status":"available"},{"id":9223372036854762522,"category":{"id":0,"name":"string"},"name":"Puff","photoUrls":["string"],"tags":[{"id":0,"name":"string"}],"status":"available"},{"id":9223372036854762533,"category":{"id":0,"name":"string"},"name":"doggie","photoUrls":["string"],"tags":[{"id":0,"name":"string"}],"status":"available"},{"id":9223372036854762539,"category":{"id":0,"name":"string"},"name":"fish","photoUrls":["string"],"tags":[{"id":0,"name":"string"}],"status":"available"},{"id":9223372036854762543,"category":{"id":0,"name":"string"},"name":"fish","photoUrls":["string"],"tags":[{"id":0,"name":"string"}],"status":"available"},{"id":9223372036854762546,"category":{"id":0,"name":"string"},"name":"fish","photoUrls":["string"],"tags":[{"id":0,"name":"string"}],"status":"available"},{"id":9223372036854762547,"category":{"id":0,"name":"string"},"name":"fish","photoUrls":["string"],"tags":[{"id":0,"name":"string"}],"status":"available"},{"id":9223372036854762566,"name":"Doggie","photoUrls":["http://example.com/photo.jpg"],"status":"available"},{"id":9223372036854762567,"name":"AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA","photoUrls":["http://example.com/photo.jpg"],"status":"available"},{"id":9223372036854762568,"name":"Doggie","photoUrls":["http://example.com/photo.jpg"],"status":"available"},{"id":9223372036854762576,"category":{"id":0,"name":"string"},"name":"fish","photoUrls":["string"],"tags":[{"id":0,"name":"string"}],"status":"available"},{"id":9223372036854762611,"category":{"id":0,"name":"string"},"name":"Puff","photoUrls":["string"],"tags":[{"id":0,"name":"string"}],"status":"available"},{"id":9223372036854762614,"name":"Doggie","photoUrls":["http://example.com/photo.jpg"],"status":"available"},{"id":9223372036854762616,"name":"AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA","photoUrls":["http://example.com/photo.jpg"],"status":"available"},{"id":9223372036854762617,"category":{"id":0,"name":"Jerry"},"name":"Mouse","photoUrls":["string"],"tags":[{"id":0,"name":"Mouse"}],"status":"available"},{"id":9223372036854762618,"name":"Doggie","photoUrls":["http://example.com/photo.jpg"],"status":"available"},{"id":9223372036854762621,"category":{"id":0,"name":"string"},"name":"doggie","photoUrls":["string"],"tags":[{"id":0,"name":"string"}],"status":"available"},{"id":9223372036854762624,"category":{"id":0,"name":"string"},"name":"fish","photoUrls":["string"],"tags":[{"id":0,"name":"string"}],"status":"available"},{"id":9223372036854762625,"category":{"id":0,"name":"SHera"},"name":"doggie","photoUrls":["string"],"tags":[{"id":0,"name":"string"}],"status":"available"},{"id":9223372036854762626,"category":{"id":0,"name":"sdfgjhk"},"name":"doggie","photoUrls":["string"],"tags":[{"id":0,"name":"string"}],"status":"available"},{"id":9223372036854762680,"category":{"id":0,"name":"string"},"name":"doggie","photoUrls":["string"],"tags":[{"id":0,"name":"string"}],"status":"available"},{"id":9223372036854762682,"name":"Doggie","photoUrls":["http://example.com/photo.jpg"],"status":"available"},{"id":9223372036854762683,"name":"AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA","photoUrls":["http://example.com/photo.jpg"],"status":"available"},{"id":9223372036854762684,"name":"Doggie","photoUrls":["http://example.com/photo.jpg"],"status":"available"},{"id":9223372036854762687,"category":{"id":0,"name":"string"},"name":"doggie","photoUrls":["string"],"tags":[{"id":0,"name":"string"}],"status":"available"},{"id":9223372036854762692,"category":{"id":0,"name":"string"},"name":"doggie","photoUrls":["string"],"tags":[{"id":0,"name":"string"}],"status":"available"},{"id":9223372036854762696,"category":{"id":0,"name":"string"},"name":"fish","photoUrls":["string"],"tags":[{"id":0,"name":"string"}],"status":"available"},{"id":9223372036854762697,"category":{"id":0,"name":"string"},"name":"doggie","photoUrls":["string"],"tags":[{"id":0,"name":"string"}],"status":"available"},{"id":216385269530624,"category":{"id":0,"name":"retrospectivity"},"name":"Tina Rolfson","photoUrls":["http://example.com/photo1.jpg","http://example.com/photo2.jpg"],"tags":[{"id":0,"name":"quality"}],"status":"available"},{"id":912167960313856,"category":{"id":0,"name":"dame"},"name":"Kay Gorczany III","photoUrls":["http://example.com/photo1.jpg","http://example.com/photo2.jpg"],"tags":[{"id":0,"name":"wardrobe"}],"status":"available"},{"id":9223372036854762701,"category":{"id":0,"name":"string"},"name":"doggie","photoUrls":["string"],"tags":[{"id":0,"name":"string"}],"status":"available"},{"id":9223372036854762702,"category":{"id":0,"name":"string"},"name":"doggie","photoUrls":["string"],"tags":[{"id":0,"name":"string"}],"status":"available"},{"id":9223372036854762707,"category":{"id":0,"name":"string"},"name":"doggie","photoUrls":["string"],"tags":[{"id":0,"name":"string"}],"status":"available"},{"id":26,"category":{"id":0,"name":"string"},"name":"doggie","photoUrls":["string"],"tags":[{"id":0,"name":"string"}],"status":"available"},{"id":9223372036854762709,"category":{"id":0,"name":"string"},"name":"Puff","photoUrls":["string"],"tags":[{"id":0,"name":"string"}],"status":"available"},{"id":222,"category":{"id":2,"name":"Beagle"},"name":"Beagle_Eagle","photoUrls":["3"],"tags":[{"id":0,"name":"Beagle_Eagle_4"}],"status":"available"},{"id":9223372036854762710,"category":{"id":0,"name":"string"},"name":"doggie","photoUrls":["string"],"tags":[{"id":0,"name":"string"}],"status":"available"},{"id":9223372036854762711,"category":{"id":0,"name":"string"},"name":"doggie","photoUrls":["string"],"tags":[{"id":0,"name":"string"}],"status":"available"},{"id":9223372036854762728,"category":{"id":0,"name":"string"},"name":"fish","photoUrls":["string"],"tags":[{"id":0,"name":"string"}],"status":"available"},{"id":9223372036854762733,"category":{"id":0,"name":"string"},"name":"fish","photoUrls":["string"],"tags":[{"id":0,"name":"string"}],"status":"available"},{"id":9223372036854762734,"category":{"id":0,"name":"string"},"name":"fish","photoUrls":["string"],"tags":[{"id":0,"name":"string"}],"status":"available"},{"id":29,"category":{"id":0,"name":"string"},"name":"doggie","photoUrls":["string"],"tags":[{"id":0,"name":"string"}],"status":"available"},{"id":9223372036854762776,"category":{"id":0,"name":"string"},"name":"Puff","photoUrls":["string"],"tags":[{"id":0,"name":"string"}],"status":"available"},{"id":24,"category":{"id":0,"name":"string"},"name":"doggie","photoUrls":["string"],"tags":[{"id":0,"name":"string"}],"status":"available"},{"id":9223372036854762785,"category":{"id":0,"name":"string"},"name":"doggie","photoUrls":["string"],"tags":[{"id":0,"name":"string"}],"status":"available"},{"id":9223372036854762793,"category":{"id":0,"name":"string"},"name":"fish","photoUrls":["string"],"tags":[{"id":0,"name":"string"}],"status":"available"},{"id":9223372036854762840,"category":{"id":0,"name":"string"},"name":"doggie","photoUrls":["string"],"tags":[{"id":0,"name":"string"}],"status":"available"},{"id":9223372036854762882,"category":{"id":0,"name":"string"},"name":"doggie","photoUrls":["string"],"tags":[{"id":0,"name":"string"}],"status":"available"},{"id":9223372036854762885,"category":{"id":0,"name":"string"},"name":"fish","photoUrls":["string"],"tags":[{"id":0,"name":"string"}],"status":"available"},{"id":77777,"category":{"id":5,"name":"Dogs"},"name":"Jack","photoUrls":["string"],"tags":[{"id":5,"name":"dog"}],"status":"available"},{"id":9223372036854763094,"category":{"id":0,"name":"string"},"name":"doggie","photoUrls":["string"],"tags":[{"id":0,"name":"string"}],"status":"available"},{"id":9223372036854763120,"category":{"id":0,"name":"string"},"name":"Puff","photoUrls":["string"],"tags":[{"id":0,"name":"string"}],"status":"available"},{"id":9223372036854763122,"name":"Doggie","photoUrls":["http://example.com/photo.jpg"],"status":"available"},{"id":9223372036854763123,"name":"AAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAAA","photoUrls":["http://example.com/photo.jpg"],"status":"available"},{"id":9223372036854763124,"name":"Doggie","photoUrls":["http://example.com/photo.jpg"],"status":"available"},{"id":99999999,"name":"UpdatedDoggie","photoUrls":["http://example.com/photo.jpg"],"status":"available"},{"id":9223372036854763129,"category":{"id":0,"name":"string"},"name":"doggie","photoUrls":["string"],"tags":[{"id":0,"name":"string"}],"status":"available"},{"id":22,"category":{"id":0,"name":"string"},"name":"doggie","photoUrls":["string"],"tags":[{"id":0,"name":"string"}],"status":"available"},{"id":27,"category":{"id":0,"name":"string"},"name":"doggie","photoUrls":["string"],"tags":[{"id":0,"name":"string"}],"status":"available"},{"id":112233,"category":{"id":30,"name":"Eq-dog"},"name":"Postman","photoUrls":["URLLink"],"tags":[{"id":10,"name":"Doberman"}],"status":"available"},{"id":9223372036854763138,"category":{"id":0,"name":"string"},"name":"fish","photoUrls":["string"],"tags":[{"id":0,"name":"string"}],"status":"available"},{"id":9223372036854763139,"category":{"id":0,"name":"string"},"name":"fish","photoUrls":["string"],"tags":[{"id":0,"name":"string"}],"status":"available"},{"id":9223372036854763140,"category":{"id":0,"name":"string"},"name":"fish","photoUrls":["string"],"tags":[{"id":0,"name":"string"}],"status":"available"}]
Veronika@LAPTOP-BJACTRKT MINGW64 ~
$ curl -X 'POST' \
  'https://petstore.swagger.io/v2/user' \
  -H 'accept: application/json' \
  -H 'Content-Type: application/json' \
  -d '{
  "id": 12345,
  "username": "newuser",
  "firstName": "John",
  "lastName": "Doe",
  "email": "johndoe@example.com",
  "password": "password123",
  "phone": "1234567890",
  "userStatus": 1
il\": \"johndoe@example.com\", \"password\": \"password123\", \"phone\": \"1234567890\", \"userStatus\": 1 }"' >> bash2.txt" -d "{ \"id\": 12345, \"username\": \"newuser\", \"firstName\": \"John\", \"lastName\": \"Doe\", \"ema
{"code":200,"type":"unknown","message":"12345"}
Veronika@LAPTOP-BJACTRKT MINGW64 ~
$
