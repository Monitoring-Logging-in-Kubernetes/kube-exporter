# kube-exporter

Here is what we are going to do.

Deploy node exporter on all the Kubernetes nodes as a daemonset. Daemonset makes sure one instance of node-exporter is running in all the nodes. It exposes all the node metrics on port 9100 on the /metrics endpoint
Create a service that listens on port 9100 and points to all the daemonset node exporter pods. We would be monitoring the service endpoints (Node exporter pods) from Prometheus using the endpoint job config. More explanation on this in the Prometheus config part.
