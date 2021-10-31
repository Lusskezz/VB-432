# PSR-7: HTTP message interfaces

This document describes common interfaces for representing HTTP messages as described in [RFC 7230](https://datatracker.ietf.org/doc/html/rfc7230) and [RFC 7231](https://datatracker.ietf.org/doc/html/rfc7231), and URIs for use with HTTP messages as described in [RFC 3986](https://datatracker.ietf.org/doc/html/rfc3986).


## References

*[RFC 2119](http://tools.ietf.org/html/rfc2119)
*[RFC 3986](https://datatracker.ietf.org/doc/html/rfc3986)
*[RFC 7230](https://datatracker.ietf.org/doc/html/rfc3986)


## Every HTTP request message has a specific form:

```
POST /path HTTP/1.1
Host: example.com

foo=bar&baz=bat
```

REQUEST HOST HEADER | REQUEST HOST COMPONENT | URI HOST COMPONENT
:--- | ---: | :---:
" | " | "
" | foo.com | "
" | foo.com | bar.com
foo.com | " | bar.com
foo.com | bar.com | baz.com
