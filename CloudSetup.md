# Choosing a cloud provider for the workshop

For those who wish to follow along during the workshop a public cloud setup is recommended for its flexibility. Any cloud provider, including one provided by your company, will do. We will demonstrate a cluster installation on digital ocean droplets as its quite similar to on-premise installations.

## Workshop setup

### Cloud instances

For the purpose of the workshop we will build a 6 node cluster containing 2 master nodes, 3 worker nodes and 1 utility node.

| Master       | Worker                      | Utility     |
|:------------:|:---------------------------:|:-----------:|
| 4 CPU cores  | 12 CPU cores                | 8 CPU cores |
| 8GB RAM     | 32GB RAM                    | 16GB RAM    |
| 80GB SSD     | 320GB SSD                   | 160GB SSD    |
| Added block storage 20GB | Added block storage 200GB | Added block storage 20GB |   

For the workshop we will use CentOS 7 images, but you are welcomed to try out any other Cloudera supported OS versions.

### Networking

Each instance needs to be connected to a private network so that inter-cluster communication doesn't go through the public internet. At most cloud providers the private networking option has to be specified and instances should be in the same zone.


### Digital Ocean toolkit

**Terraform**

* automates droplet creating and destroying
* utilizes digital ocean v2 api
* requires a generated token for access

To install Terraform take a look at these links:

https://www.terraform.io/intro/getting-started/install.html
https://www.digitalocean.com/community/tutorials/how-to-use-terraform-with-digitalocean



### Other alternatives outside the scope of the workshop

**Cloudera Director**

* simplest solution for cloud installations in AWS, Azure and Google Cloud Platform
* flexible self service cloud deployment solution
* installs supported Cloudera clusters from scratch to production ready systems
* extensible open framework

Please take a look at these links:

https://www.cloudera.com/products/product-components/cloudera-director.html
