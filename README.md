<center>![Average internet Speed](https://i.ibb.co/vXGD78L/Capture.png)</center>

In an era where the average internet speed is constantly growing(with 5G and other new available technologies) is Google speed insights (or alternatives) still useful?

For me the answer is no, therefore I've chosen to block those User Agents in .htaccess so no one can act like a smart ass pointing out an error that I was to lazy to fix on one of my websites.



    RewriteEngine On
    RewriteCond %{HTTP_USER_AGENT} ^.*(Chrome-Lighthouse|GTmetrix).*$ [NC]
    RewriteRule .* - [F,L]
    RewriteCond %{HTTP_USER_AGENT} ^Ping[^dom\.com_bot.*] [OR]
    RewriteRule ^.* - [F,L]
