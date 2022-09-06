# Simple TLS 1.2

## Description
Custom simple TLS implementation in python. The implementation of TLS 1.2 was based on [The Illustrated TLS 1.2 Connection](https://tls12.xargs.org/). To simplify, only 1 cipher suite is supported, and the certificate of the server is not verified.

## Overview
### Supported TLS Cipher Suite
The server only supports one of the TLS cipher suites on [TLS Cipher Suite Registry](https://www.iana.org/assignments/tls-parameters/tls-parameters.xhtml#tls-parameters-4).

|                |                                  |
|----------------|----------------------------------|
| IANA Name      | TLS_DHE_RSA_WITH_AES_128_CBC_SHA |
| Hex Code       | 0x00, 0x33                       |
| Key Exchange   | DHE                              |
| Authentication | RSA                              |
| Encryption     | AES 128 CBC                      |
| Hash           | SHA1                             |

Note: CBC and SHA1 has been proven to be vulnerable/insecure. Therefore, this cipher is weak and not recommended for use.

### Smple TLS 1.2 Steps:
1. Hello

