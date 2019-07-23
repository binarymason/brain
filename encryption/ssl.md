Secure Socket Layer uses Public Key Infrastructure (PKI).

It works like this:

* Client sends a ClientHello message to the server
* Server sends a ServerAck message to the client along with its public key
* (optional) Client asks a Certificate Authority that the Server's public key fingerprint is correct
* Client generates a secret for symmetrical encryption, encrypts **that** with Server's public key and sends to Server
* Server decrypts secret with its private key
* Now both Client and Server share the same symmetric key to use for encrypted communication.
