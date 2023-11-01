# monitoring

![image](https://github.com/ivorobey/monitoring_scheme/blob/main/mon_scheme.jpg)

- Kubernetes: A platform for managing and scaling containerized applications. Used to manage the deployment of all tools in the cluster.

- Grafana: a data visualization tool used to create dashboards and present metrics and logs from Prometheus, Loki, etc.

- Prometheus: a monitoring and alerting system that collects metrics from applications and infrastructure, then analyzes them and generates alerts when specified rules are violated. Prometheus can send metrics to Cortex via remote_write.

- Cortex: a horizontally scalable platform for storing and querying metrics that uses Minio as storage for its data. Cortex can also be used to aggregate metrics from multiple sources.

- Loki: a system running as StatefulSet in Kubernetes and serving to collect and store application and infrastructure logs. Loki sends logs to Minio buckets for long-term storage.

- Promtail runs as a DaemonSet in Kubernetes and collects logs from applications and infrastructure. Promtail sends logs to Loki for indexing and storage. 
  Promtail can be configured to collect logs from various sources, such as log files, syslog, journald and others.

- Tempo: a trace collection and storage system that uses Minio as storage for its data. Tempo can also be used for trace search and analysis.
  Tempo runs as a StatefulSet in Kubernetes and is used to store traces over the long term. Tempo uses Minio buckets to store traces.
  Receiver is the tempo component that is responsible for receiving and processing metrics
  
- Minio is an object repository that can be used to store data collected from various monitoring sources such as Cortex and Tempo. Minio provides long-term data storage   and also provides data backup and recovery.
  Minio is deployed as a StatefulSet in Kubernetes, which provides fault resistance and high availability

- Elasticsearch is a search and analytics engine used to store, search, and analyze data. 
  Logstash is the tool used to collect, process, and report data to Elasticsearch

