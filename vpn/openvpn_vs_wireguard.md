# OpenVPN vs Wireguard

The purpose of this guide is to set a framework for assessing different remote access protocols for a small/mid size company. Any improvment suggestion is welcome!

## Objective
A secure, reliable, and easily-managed remote access solution for every employee.

## Method
We are going to compare OpenVPN and Wireguard two protocols in the following categories:

* Security - Strong ciphers 
* Performance - Low networking overhead
* Availability - Failover mechanism
* Management - Directory integration

Each protocol gets 1 point for winning or meeting a category.

|                               |                                  OpenVPN                                 |     Wireguard     |
|-------------------------------|:------------------------------------------------------------------------:|:-----------------:|
|### **Security**               |                                                                          |                   |
| encryption and authentication | AES Blowfish Camellia ChaCha20 Poly1305 DES Triple DES GOST 28147-89 SM4 | ChaCha20 Poly1305 |
|                       hashing |                     MD5 MD4 SHA-1 SHA-2 MDC-2 BLAKE2                     |  BLAKE2 SipHash24 |
|                   key sharing |                       RSA  DSA  X25519  Ed25519 SM2                      |  Curve25519 HKDF  |
|       Perfect Forward Secrecy |                                    yes                                   |        yes        |
|                   **Verdict** |                                     1                                    |         1         |
|                               |                                                                          |                   |
|### **Performance**            |                                                                          |                   |
|                     OSI Layer |                                     7                                    |         3         |
|                   **Verdict** |                                     0                                    |         1         |
|                               |                                                                          |                   |
|### **Availability**           |                                                                          |                   |
|               Server failover |                                    yes                                   |         no        |
|                   **Verdict** |                                     1                                    |         0         |
|                               |                                                                          |                   |
|### **Management**             |                                                                          |                   |
| Directory service integration |                                    yes                                   |         no        |
|                   **Verdict** |                                    1                                     |         0         |
|                               |                                                                          |                   |
|### **Final score**            |                                     3                                    |         2         |
|                               |                                                                          |                   |
|                               |                                                                          |                   |
|                               |                                                                          |                   |

## Conclusion
For the time being OpenVPN makes perfect sense for any sysadmin out there to quickly set up remote access tunnel and integrate with existing directory service. On the other end, Wireguard may offer great networking performance but the lack of ability to integrate with directory servies creates a management overhead oftehn becomes a security issue down the road (Hint: Colonial Pipeline).  
