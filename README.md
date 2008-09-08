
# http-twiddle -- send & twiddle & resend HTTP requests

This is a program for testing hand-written HTTP requests. You write
your request in an Emacs buffer (using http-twiddle-mode) and then
press `C-c C-c' each time you want to try sending it to the server.
This way you can interactively debug the requests. To change port or
destination do `C-u C-c C-c'.

The mode is activated by `M-x http-twiddle-mode' or automatically
when opening a filename ending with .http-twiddle.

The request can either be written from scratch or you can paste it
from a snoop/tcpdump and then twiddle from there.

See the documentation for the `http-twiddle-mode' and
`http-twiddle-mode-send' functions below for more details and try
`M-x http-twiddle-mode-demo' for a simple get-started example.


## Examples

If the Content-Length header is not written out (like in the examples below) it'll be added automatically on send.

### GET:
GET /user/bob/ HTTP/1.1
Host: example.com
[blank line here]

### POST:
POST /user/create/ HTTP/1.1
Host: example.com
Content-Type: text/xml
Connection: close

<user><name>Bob</name><email>bob@example.com</email></user>


## About

Version 1.0 was written by Luke Gorrie <luke@synap.se> in February 2006 and released to the public domain.

Extended and maintained by Hasan Veldstra <hassy@12monkeys.co.uk> since September 2008.

Homepage: <http://github.com/hassy/http-twiddle/tree/master>
