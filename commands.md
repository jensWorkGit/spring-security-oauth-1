mvn clean install

keytool -genkeypair -alias mytest -keyalg RSA -keypass mypass -keystore mytest.jks -storepass mypass

# export public key (only works in git bash)
keytool -list -rfc --keystore mytest.jks | openssl x509 -inform pem -pubkey