# Elastic stack

Deploy and manage Elastic stack.

## Deploy

1. Elasticsearch - `kubectl apply -k elasticsearch`
2. Run the following command to generate password automatically

    `kubectl exec -it $(kubectl get pods -n elastic | grep elasticsearch-client | sed -n 1p | awk '{print $1}') -n elastic -- bin/elasticsearch-setup-passwords auto -b`

3. Copy `elastic` password generated before and add it as secret in `kibana/secret.yml` (encode it in base64)
4. Kibana - `kubectl apply -k kibana`

## Enable ingress

1. Change subdomain for kibana and elasticsearch (optional) with yours in `ingress` dir.
2. Apply: `kubectl apply -k ingress`
