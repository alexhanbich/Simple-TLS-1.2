# TLS from scratch

## Description
custom mini TLS implementation in python

## Overview
Cipher suite used:
- key exchange algorihtm: Diffie–Hellman key exchange
- signiture algorithm to sign certificates: SHA3-256
- symmetric encryption algorithm: AES-128 CBC
- HMAC algorithm: HMAC SHA-1

TLS Steps:
1. client -> server: Hello / Key share
2. server -> client: Key share / Certificate / Finished
3. client <-> server: encrypted communication
