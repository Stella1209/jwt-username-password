# Spring Security JWT - Username & Password

This is a continuation of my [previous tutorial](https://github.com/danvega/jwt) on JSON Web Tokens (JWT) with Spring Security. 

A lot of the feedback I received from that you really enjoyed it, but you also wanted a way to remove Http Basic authentication 
and replace it with a username + password authentication at the controller level. This tutorial will cover how to do that. 

## Generating RSA key pair

make directory `mkdir src/main/resources/certs`

go into the directory `cd src/main/resources/certs`

generate priavte key `openssl genrsa -out keypair.pem 2048`

extract public key from private key`openssl rsa -in keypair.pem -pubout -out public.pem`