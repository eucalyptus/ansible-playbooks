MongoDB EC2/Eucalyptus deployment example
=========================================
Built against Ansible 1.1 

This sample playbook demonstrates provisioning of a MongoDB replicaset in Eucalyptus or EC2.  
It uses ephemeral space on instances as the db store.  Use a minimum of two instances, the playbook will scale accordingly.

To execute this playbook, follow these steps:

* Set environmental variables: EC2_URL (if using Eucalyptus or specific endpoint), EC2_ACCESS_KEY (your Euca or AWS access key) and EC2_SECRET_KEY (your Euca or AWS secret key)
* Edit ```mongodb-eucalyptus-ec2.yml``` and alter cloud-specific variables in the first play: ```keypair```, ```instance_type```, ```security_group```, ```image``` and ```count```. Check Ansible's module pages for more ec2-related options.
* Using your private key, run the playbook like so: ```ansible-playbook mongodb-eucalyptus-ec2.yml -v --private-key=/path/to/my/key.pri```
