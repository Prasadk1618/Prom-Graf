### Prometheus Grafana SetUp On Amazon Linux..!!

## Prometheus Installiton..!!

- Excute Following Command

```bash
sudo tee /etc/yum.repos.d/prometheus.repo <<EOF
[prometheus]
name=Prometheus
baseurl=https://packagecloud.io/prometheus-rpm/release/el/7/x86_64
repo_gpgcheck=1
enabled=1
gpgkey=https://packagecloud.io/prometheus-rpm/release/gpgkey https://raw.githubusercontent.com/lest/prometheus-rpm/master/RPM-GPG-KEY-prometheus-rpm
gpgcheck=1
metadata_expire=300
EOF
```

- Update System

```bash
sudo yum update -y
```

- Install Node-Exporter

```bash
sudo yum -y install prometheus2 node_exporter

rpm -qi prometheus2


```

- Start Prometheus Node_exporter

```bash
sudo systemctl start prometheus node_exporter
```

- add port 9090 in security group



### Grafana Setup..!!

- Command For Install Grafana

```bash
sudo yum install -y https://dl.grafana.com/oss/release/grafana-10.0.3-1.x86_64.rpm
```

- Copy Your Public Ip :3000 And Hit Your Browser
