# My Pentest Check List

> Một vài note nhỏ cho bản thân 

> Giảm thởi gian ngu ngốc trong cuộc thi

> Mong sẽ giúp ích được cho các bạn

## Server

### Discovering
1. File thông dụng: /robots.txt,.git, .htaccess, .htpasswd
2. Các url con: /images, /js, /css
3. Cookie, Console, Network
4. Backup file: ~,bak,zip,bzr
4. Http header: 
    Server
    * X-Powered-By: PHP
    * X-AspNet-Version: ASP.Net
    * x-cache, x-status, hit/miss: web cache
    * X-Application-Context: spring boot
5. Dirsearch, Dirbuster, nmap 

```py dirsearch.py -u <url> -e * ```

6. Weak password: `admin`, `123456`

### SQL Injection
Đối với những website chỉ có login, register, truy xuất dữ liệu từ database, ta có thể test thử: Có thể là ở các khung input, cookie, user-gent,...
    `3' or 1=1 -- +`
    `3' or 1=1 #`
    `3' or 1=1 /*`
    `3' or '1'='1`
    `3' or sleep(1) -- +`
    `3' union select * from user -- +`
### NoSQL Injection
### XSS
### LFI, RFI
### Command Injection
### SSTI
1. Test `{{4*4}}[[5*5]]`
### XXE


## Client
