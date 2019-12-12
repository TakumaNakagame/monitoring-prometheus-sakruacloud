# 🌸Monitoring Prometheus SAKURACloud🌸
Easy setup for Monitoring SAKURA Cloud with Prometheus on Docker-Compose.

In use : https://github.com/sacloud/sakuracloud_exporter

## Required
- Running Docker
- Running Docker-Compose
- [Signup SAKURA Cloud](https://cloud.sakura.ad.jp/)

## How to use
### 1. Get SAKURA Cloud Token/Secret
Access to [https://secure.sakura.ad.jp/cloud/#!/apikey/top/](https://secure.sakura.ad.jp/cloud/#!/apikey/top/) .
Generate and copy for Token/Secret.

### 2. Clone repository
Clone for this repository.
```
cd WORKING_DIR
git clone https://github.com/TakumaNakagame/monitoring-prometheus-sakruacloud
cd monitoring-prometheus-sakruacloud
```

### 3. Insert Token/Secret
Paste the copied Token and Secret into `docker-compose.yml`

```
command: 
    - --token=[TOKEN_TEXT]
    - --secret=[SECRET_TEXT]
```

### 3. Running containers
Run containers with Prometheus and SAKURA Cloud Exporter.

```
docker-compose up -d
```

### 4. Connecting to Prometheus
Connecting to Prometheus GUI.

http://localhost:9090/