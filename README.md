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

### Arguments forwarded to HTTPie

1. --verbose
2. --timeout

### Limitations

Currently it can only translate headers and data.
