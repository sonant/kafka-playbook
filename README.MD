HOW TO USE
----------

```bash
ansible-playbook -i hosts.yaml  kafka.yaml -k -K -v
```

Inventory file is: hosts.yaml

If you want using ssl and please change group_vars file - all:

Create the Truststore and Keystore

```bash
roles/kafka/files/keys/kafka.truststore.jks
roles/kafka/files/keys/kafka.keystore.jks
```

```yaml
ssl_client_auth: yes
ssl_keystore_password: 111
ssl_truststore_password: 111
ssl_key_password: 111  #if required
```

REQUIREMENTS
------------

- zookeeper
