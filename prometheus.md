global:
  scrape_interval: 5s

alerting:
  alertmanagers:
    - static_configs:
        - targets:
            - "127.0.0.1:9093"

rule_files:
  - "alert.rules.yml"

scrape_configs:
  - job_name: 'prometheus'
    static_configs:
      - targets: ['127.0.0.1:9090']

  - job_name: 'node_exporter'
    static_configs:
      - targets: ['127.0.0.1:9']
