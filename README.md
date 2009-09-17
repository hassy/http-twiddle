
# http-twiddle

This Emacs addon is useful for interactive testing and debugging hand-written HTTP requests:

1. Activate `http-twiddle-mode` with `M-x`.
2. Write your request.
3. `C-c C-c` (re)sends the request.

(`C-u C-c C-c` to change the destination or port.)

The request can either be written from scratch or you can paste it
from a snoop/tcpdump and then twiddle from there.

The mode will also activate automatically when opening a filename ending with `.http-twiddle`.

## Examples

Try `M-x http-twiddle-mode-demo` in Emacs for a simple get-started example.

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

Extended and maintained by Hasan Veldstra <hasan.veldstra@gmail.com> since September 2008.

Homepage: <http://github.com/hassy/http-twiddle/tree/master>
