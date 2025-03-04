# blood-bank-system-in-php has Cross Site Scripting vulnerability in AB+.php

## supplier 
https://code-projects.org/blood-bank-system-in-php-with-source-code/
## Vulnerability file
AB+.php
## describe
There is an  Cross Site Scripting vulnerability in blood-bank-system-in-php  in AB+.php. Control parameter: $Bloodname

A malicious attacker can use this vulnerability to obtain administrator login credentials or phishing websites

## code analysis

In AB+.php，get $row['Bloodname'], and echo it in no filter.

![Image](https://github.com/user-attachments/assets/41874d32-5fc3-4d2c-a51c-55a510b8cbb6)

## POC

```
GET /Blood/AB+.php HTTP/1.1
Host: bloodbankmgmtsystem
Cache-Control: max-age=0
Upgrade-Insecure-Requests: 1
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/122.0.6261.112 Safari/537.36
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.7
Accept-Encoding: gzip, deflate, br
Accept-Language: zh-CN,zh;q=0.9
 Connection: close


```

**Result**

![Image](https://github.com/user-attachments/assets/d0b56620-7c36-4871-8183-22c49d8953a8)

![Image](https://github.com/user-attachments/assets/4dfaca7a-b96c-4933-bbed-e2ab6365f58b)
