HOW TO USE
----------

Inventory file is: hosts.yaml

```bash
ansible-playbook -i hosts.yaml  kafka.yaml -k -K -v
```

If you want using ssl:

Create the Truststore and Keystore files:

```bash
roles/kafka/files/keys/kafka.truststore.jks
roles/kafka/files/keys/kafka.keystore.jks
```

Set vars in group_vars file - 'all':

```yaml
ssl_client_auth: yes
ssl_keystore_password: 111
ssl_truststore_password: 111
ssl_key_password: 111  #if required
```

### Simple ACL support

Now it support consumers acl option:

```yaml
kafka_acl_producers: 
  - { topic: "demo", user: "demo" }
  - { topic: "demo", user: "demo2" }
```

REQUIREMENTS
------------

- zookeeper
