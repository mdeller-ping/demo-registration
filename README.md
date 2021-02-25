# demo-registration

## build the image from source and run as a container locally

``docker build -t demo-registration .``

``docker run -p 80:80 demo-registration``

## deploy from docker hub and run locally

``docker run -p 80:80 michaeldeller/demo-registration``

## deploy from docker hub and expose with load balancer on kubernetes

``kubectl create deployment --image=michaeldeller/demo-registration friendlyname-demo-registration``

``kubectl expose deployment friendlyname-demo-registration --port=80 --target-port=80 --type=LoadBalancer --name=friendlyname-demo-registration-lb``