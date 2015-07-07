## Curlie

Curlie is a simple translator between curl and HTTPie.

### Requirements

1. Python2 or Python3
2. HTTPie

### Usage

1. Download curlie, put it on your PATH (save it under the name xcurl)
2. Open the network tab in chrome devtools and right click / Copy as cURL on a request
3. Open your terminal type 'x' then paste the contents of your clipboard
4. Hit enter

By default it will print out the command that it will call, this behaviour can be disabled by passing `-q` or `--quiet` to curlie.

### Terminalshot

    $ xcurl 'http://www.google.com' -H 'User-Agent: Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/42.0.2311.135 Safari/537.36' --verbose                                                                       [0]
    
    http GET http://www.google.com 'User-Agent: Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/42.0.2311.135 Safari/537.36' --verbose
    
    GET / HTTP/1.1
    Accept: */*
    Accept-Encoding: gzip, deflate
    Host: www.google.com
    User-Agent:  Mozilla/5.0 (X11; Linux x86_64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/42.0.2311.135 Safari/537.36
    
    
    
    HTTP/1.1 302 Found
    Alternate-Protocol: 80:quic,p=0
    Cache-Control: private
    Content-Length: 259
    Content-Type: text/html; charset=UTF-8
    Date: Tue, 07 Jul 2015 17:20:19 GMT
    Location: http://www.google.co.uk/
    Server: GFE/2.0
    
    <HTML><HEAD><meta http-equiv="content-type" content="text/html;charset=utf-8">
    <TITLE>302 Moved</TITLE></HEAD><BODY>
    <H1>302 Moved</H1>
    The document has moved
    <A HREF="http://www.google.co.uk/">here</A>.
    </BODY></HTML>

### Arguments forwarded to HTTPie

1. --verbose
2. --timeout

### Limitations

Currently it can only translate headers and data.
