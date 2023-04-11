# qtest
q type of test
# QComb - generator of random combinations of characters.
Mostly used for passwords.

(v1.1)

### Prerequisites:
- Linux, Windows (developed and tested with Linux, tested with Windows IIS. It may work in other OS environments too because the main thing is Web server and PHP)
- PHP >= 7.2
- PHP extensions:
  - php-xml (for html & xml work)
  - php-gmp (for arbitrary-length integers work)

- a web server (tested with Apache, IIS)
- unsupported browsers:
  - Internet Explorer

### Installation:

1. Unpack the archive into web server root or some other place which is accessible by the web server (additional web server configuration may be necessary in the latter case).
2. Set recursively read&write rights for the web server user (apache, www-data, etc.) on the directory (chown -R).
  - If your Linux uses SELinux (Red Hat like), use such commands:
```
chcon -R -t httpd_sys_content_t /path-to web-content/qcomb
chcon -R -t httpd_sys_rw_content_t /path-to web-content/qcomb
```
(The above applies only to writing the log file, if you don't use that option you will never need it.)

### Access the web interface by the following link:

http(s)://IP_OR_SERVER_ADDRESS/qcomb
