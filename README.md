# Commands to genrate the .jks file from the private & public key(file type: PEM)

openssl pkcs12 -export -in public_key_PEM_file -out temp_PKCS_file.pkcs12 -name pkcs_name -inkey private_key_PEM_file

keytool -v -importkeystore -srckeystore temp_PKCS_file.pkcs12 -srcstoretype PKCS12 -destkeystore JKS_file.jks -deststoretype JKS


Note:- use the same password for both the commands when it prompts .
  The generated JKS file can be used for ssl connection or hosting the server as https.
