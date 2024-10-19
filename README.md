# Работа с git и bash  
bash1.txt  

1) cd ~
2) basename "$PWD"
3) mkdir test1
4) cd test1
5) touch 1 2 3
6) ls
7) cd ~
8) mkdir test2
9) rmdir test2
10) rm ~/test1/2
11) mkdir test3 touch ~/test3/file1 ~/test3/file2
12) rm -r test3
13) mkdir test4
14) mv ~/test1/1 ~/test1/3 ~/test4/
15) echo -e "line\nline\nline" >> ~/test4/1
16) cat ~/test4/1
17) echo -e "line\nline\nline" >> ~/test4/3
18) cat ~/test4/1 ~/test4/3
19) nano ~/test4/1


bash2.txt 

1)cd ~ echo "cd ~" >> bash2.txt
2)mkdir test3 echo "mkdir test3" >> bash2.txt
3) echo -e "row1\nrow2\nrow3\nrow4" > ~/test3/4
echo -e "row1\nrow2\nrow3\nrow4" > ~/test3/5
echo -e "row1\nrow2\nrow3\nrow4" > ~/test3/6
echo 'echo -e "row1\nrow2\nrow3\nrow4" > ~/test3/4' >> bash2.txt
echo 'echo -e "row1\nrow2\nrow3\nrow4" > ~/test3/5' >> bash2.txt
echo 'echo -e "row1\nrow2\nrow3\nrow4" > ~/test3/6' >> bash2.txt
4) grep "row2" ~/test3/5
echo 'grep "row2" ~/test3/5' >> bash2.txt
5) grep -r "row" ~/test3
echo 'grep -r "row" ~/test3' >> bash2.txt
6) grep -c "row" ~/test3/6
echo 'grep -c "row" ~/test3/6' >> bash2.txt
7) find ~/test3 -name "5"
echo 'find ~/test3 -name "5"' >> bash2.txt
8) find ~/test3 -name "5" -delete
echo 'find ~/test3 -name "5" -delete' >> bash2.txt
9) echo "test" >> ~/test3/4
echo 'echo "test" >> ~/test3/4' >> bash2.txt
10) sed -i 's/test/fail/g' ~/test3/4
echo 'sed -i "s/test/fail/g" ~/test3/4' >> bash2.txt
11) echo "test" >> ~/test3/4
echo 'echo "test" >> ~/test3/4' >> bash2.txt
12) ps aux
echo "ps aux" >> bash2.txt
13)  kill 666
echo "kill 666" >> bash2.txt
14) ping rusau.net
echo "ping rusau.net" >> bash2.txt
15) ping -c 5 rusau.net
echo "ping -c 5 rusau.net" >> bash2.txt
16) curl -X 'GET' 'https://petstore.swagger.io/v2/pet/findByStatus?status=available' -H 'accept: application/json'
echo 'curl -X "GET" "https://petstore.swagger.io/v2/pet/findByStatus?status=available" -H "accept: application/json"' >> bash2.txt
17) curl -X 'POST' \
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
}'
echo 'curl -X "POST" "https://petstore.swagger.io/v2/user" -H "accept: application/json" -H "Content-Type: application/json" -d "{ \"id\": 12345, \"username\": \"newuser\", \"firstName\": \"John\", \"lastName\": \"Doe\", \"email\": \"johndoe@example.com\", \"password\": \"password123\", \"phone\": \"1234567890\", \"userStatus\": 1 }"' >> bash2.txt
