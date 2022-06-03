# ELK-setup

Install elastic operator with helm

helm repo add elastic https://helm.elastic.co
helm repo update
helm install elastic-operator elastic/eck-operator -n elastic-system --create-namespace


Then apply elastic_kibana.yaml, followed by filebeat.yaml and logstash.yaml.

logstash.yaml has the setup script which is run by a job, to setup the indexes, index rollover and retention, etc.