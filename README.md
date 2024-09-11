# cp-oauth

### create secrets

```bash
kubectl create secret generic credential \
--from-file=plain-users.json=secrets/creds-kafka-sasl-users.json \
--from-file=digest-users.json=secrets/creds-zookeeper-sasl-digest-users.json \
--from-file=digest.txt=secrets/creds-kafka-zookeeper-credentials.txt --namespace confluent 
```

```bash
kubectl create secret generic mycustomtruststore --from-file=truststore.jks=./jks/truststore.jks -n confluent
```


```bash
kubectl create -n confluent secret generic oauth-jass --from-file=oauth.txt=secrets/oauth_jaas.txt
```

```bash
kubectl create secret generic cacert --from-file=cacerts.pem=./ca/cacerts.pem -n confluent
```

```bash
kubectl create secret generic mds-token \
--from-file=mdsPublicKey.pem=secrets/mds-publickey.txt \
--from-file=mdsTokenKeyPair.pem=secrets/mds-tokenkeypair.txt \
--namespace confluent
```

```bash
kubectl create -n confluent secret generic oauth-jass --from-file=oauth.txt=secrets/oauth_jaas.txt
```
