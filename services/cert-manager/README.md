# Cert Manager

Deploy and manage `cert-manager`.

## Requirements for issuer

* Add AWS credentials in secret file and prod file
* Change DNS zones in prod file

## Deploy

* Cert Manager: `kubectl apply -f deploy-<VERSION>.yml`

## Deploy issuer

* `kubectl apply -k issuer/`
