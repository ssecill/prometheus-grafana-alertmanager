# prometheus-grafana-alertmanager

* helm repo add bitnami https://charts.bitnami.com/bitnami
* helm install grafana bitnami/grafana --set service.type=LoadBalancer 
  http://grafana.secil.tech:3000/login
* helm install prometheus-operator bitnami/prometheus-operator --set prometheus.service.type=LoadBalancer 
  http://pr.secil.tech:9090/graph
* helm upgrade prometheus-operator bitnami/prometheus-operator  --reuse-values --set alertmanager.service.type=LoadBalancer
  http://pralert.secil.tech:9093/#/alerts

* https://webhook.site/#!/0508e5d8-3afd-418c-a159-adec890158d5/069c49fb-1286-4b2c-81b2-abf33db945d2/1
