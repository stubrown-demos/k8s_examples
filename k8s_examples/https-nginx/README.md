* Simple setup to create a NGINX server with certs 

_You need to ensure the key and cert are created in advance_

kubectl create secret tls nginxsecret --key certs/nginx.key --cert certs/nginx.crt

kubectl create configmap nginxconfigmap --from-file=default.conf

kubectl create -f nginx-app.yaml
