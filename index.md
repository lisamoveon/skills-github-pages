---
title: Welcome to my blog!
---

If you want to access a WebDAV repository across a non-secure network, Oxygen XML Editor allows you to
load and save the documents over the HTTPS protocol (if the server understands this protocol) so that any
data exchange with the WebDAV server is encrypted.
When a WebDAV repository is first accessed over HTTPS, the server hosting the repository will present a
security certificate as part of the HTTPS protocol, without any user intervention. Oxygen XML Editor will 
use this certificate to decrypt any data stream received from the server. For the authentication to succeed
you should make sure the security certificate of the server hosting the repository can be read by Oxygen
XML Editor. This means that Oxygen XML Editor can find the certificate in the key store of the Java Runtime
Environment where it runs. You know the server certificate is not in the JRE key store if you get the error No 
trusted certificate found when trying to access the WebDAV repository.

Troubleshooting HTTPS
--------------------------

If Oxygen XML Editor cannot connect to an HTTPS-capable server and an error message appears stating that
it is "unable to find a valid certification path to the requested target", the HTTPS server is most likely either
configured to use a self-signed certificate or to use a certificate issued by an unknown authority that the Java 
Runtime Environment (JRE) used by Oxygen XML Editor does not trust.
