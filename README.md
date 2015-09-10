STEPS
#####
GENERAR CSR
===========
```sh
openssl req -new -newkey rsa:2048 -nodes -keyout domain.key -out domain.csr
```
SE SUBE EL CSR AL PROVEEDOR
===========================
SE VALIDA Y NOS GENERA UN CRT
=============================

PASAR LA KEY A PEM
==================
```sh
openssl rsa -in domain.key -text > domain.private.pem
```

PASAR EL CRT A PEM
==================
```sh
openssl x509 -inform PEM -in domain.crt > domain.public.pem
```
SEE CERTS
=========
```sh
openssl s_client -showcerts -connect domain.es:443
 ```
