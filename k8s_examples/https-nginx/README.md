* Simple setup to create a NGINX server with certs 

kubectl create secret tls nginxsecret --key nginx.key --cert nginx.crt

kubectl create configmap nginxconfigmap --from-file=default.conf

kubectl create -f nginx-app.yaml
