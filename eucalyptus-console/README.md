Eucalyptus User Console EC2/Eucalyptus deployment
=================================================

Useful for testing and development.

Launch with:

```ansible-playbook eucalyptus-userconsole-ec2.yml -v --private-key=/home/user/myprivate.key```

You can override some of the vars using --extra-vars parameter (to define the image or console version, for example:

```ansible-playbook eucalyptus-userconsole-ec2.yml -v --private-key=/home/lwade/.euca/eurocloud/lwade-admin/lwade.key --extra-vars="image=emi-C04539F3 euca_version=3.3 console_version=3.3.0"```
