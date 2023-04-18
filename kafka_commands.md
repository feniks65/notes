# Apache Kafka Daily Commands

### Start ZooKeeper Server

```bash
zookeeper-server-start.sh /path/to/zookeeper.properties
```

### Start Kafka Broker

```bash
kafka-server-start.sh /path/to/server.properties
```

### Stop ZooKeeper Server

```bash
zookeeper-server-stop.sh
```

### Stop Kafka Broker

```bash
kafka-server-stop.sh
```

### Create Topic

```bash
kafka-topics.sh --create --topic my_topic --bootstrap-server localhost:9092 --partitions 1 --replication-factor 1
```

### List Topics

```bash
kafka-topics.sh --list --bootstrap-server localhost:9092
```

### Describe Topic

```bash
kafka-topics.sh --describe --topic my_topic --bootstrap-server localhost:9092
```

### Delete Topic

```bash
kafka-topics.sh --delete --topic my_topic --bootstrap-server localhost:9092
```

### Produce Messages

```bash
kafka-console-producer.sh --topic my_topic --bootstrap-server localhost:9092
```

### Consume Messages

```bash
kafka-console-consumer.sh --topic my_topic --from-beginning --bootstrap-server localhost:9092
```

## Consumer Groups

### List Consumer Groups

```bash
kafka-consumer-groups.sh --list --bootstrap-server localhost:9092
```

### Describe Consumer Group

```bash
kafka-consumer-groups.sh --describe --group my-group --bootstrap-server localhost:9092
```

### Reset Consumer Group Offsets

```bash
kafka-consumer-groups.sh --reset-offsets --to-earliest --group my-group --topic my_topic --execute --bootstrap-server localhost:9092
```

### Dump Logs

```bash
kafka-dump-log.sh --files /var/log/log.log
```

### Check Kafka Broker APIs

```bash
kafka-broker-api-versions.sh --bootstrap-server localhost:9092
```

### Check Under-replicated Partitions

```bash
kafka-topics.sh --describe --under-replicated-partitions --bootstrap-server localhost:9092
```

