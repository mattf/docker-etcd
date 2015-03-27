# [etcd](https://github.com/coreos/etcd/) image for Docker

This image only provides a single etcd instance configured to work as
a single instance deployment.

# Build

* ```docker build -t <name>/etcd .```

# Run

* ```sudo docker run -p 4001:4001 --name etcd -d --restart=always <name>/etcd```

# Test

* ```curl -L http://127.0.0.1:4001/v2/keys/first -XPUT -d value="1st"```
* ```curl -L http://127.0.0.1:4001/v2/keys/first```
