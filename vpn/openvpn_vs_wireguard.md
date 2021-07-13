# OpenVPN vs Wireguard

The purpose of this guide is to set a framework for assessing different remote access protocols for a small/mid size company. Any improvment suggestion is welcome!

## Objective
A secure, reliable, and easily-managed remote access solution for every employee.

We are going to compare OpenVPN and Wireguard two protocols in the following categories:

* Security - Strong ciphers 
* Performance - Low networking overhead
* Availability - Failover mechanism
* Management - Directory integration

Each protocol gets 1 point for winning a category.

|                               |                                  OpenVPN                                 |     Wireguard     |
|-------------------------------|:------------------------------------------------------------------------:|:-----------------:|
|**Security**                   |                                                                          |                   |
| encryption and authentication | AES Blowfish Camellia ChaCha20 Poly1305 DES Triple DES GOST 28147-89 SM4 | ChaCha20 Poly1305 |
|                       hashing |                     MD5 MD4 SHA-1 SHA-2 MDC-2 BLAKE2                     |  BLAKE2 SipHash24 |
|                   key sharing |                       RSA  DSA  X25519  Ed25519 SM2                      |  Curve25519 HKDF  |
|       Perfect Forward Secrecy |                                    yes                                   |        yes        |
|                       Verdict |                                    tie:1                                 |        tie:1      |
|                               |                                                                          |                   |
| **Performance**               |                                                                          |                   |
|                     OSI Layer |                                     7                                    |         3         |
|                       Verdict |                                   lose:0                                 |        win:1      |
|                               |                                                                          |                   |
| **Availability**              |                                                                          |                   |
|               Server failover |                                    yes                                   |         no        |
|                       Verdict |                                    win:1                                 |        lose:0     |
|                               |                                                                          |                   |
| **Management**                |                                                                          |                   |
| Directory service integration |                                    yes                                   |         no        |
|                       Verdict |                                    win:1                                 |        lose:0     |
|                               |                                                                          |                   |
| **Final score**               |                                     3                                    |         2         |
|                               |                                                                          |                   |
|                               |                                                                          |                   |
|                               |                                                                          |                   |
