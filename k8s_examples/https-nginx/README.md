* Simple setup to create a NGINX server with certs 

_You need to ensure the key and cert are created in advance_

kubectl create secret tls nginxsecret --key certs/key.pem --cert certs/cert.pem

kubectl create configmap nginxconfigmap --from-file=default.conf

kubectl create -f nginx-app.yaml

_remember the key needs to be installed on laptop/mac to work, if your not using DNS, use hosts file on mac and remember to open up node port number on AWS etc
