Creating certificate commands after creating https.config

1. openssl req -config https.config -new -out csr.pem
2. openssl x509 -req -days 365 -extfile https.config -extensions v3_req -in csr.pem -signkey key.pem -out https.crt
3. openssl pkcs12 -export -out https.pfx -inkey key.pem -in https.crt -password pass:<<Password>>
4. Then trust the certificate from the browse





Application:
1. Created certificate for local development
2. 
