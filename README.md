# jenkinswithecsagent

provision infra using using awscli  -->

aws cloudformation deploy  --tempate-file aimdek.yaml --stack-name <stack_name>  --capabilities CAPABILITY_NAMED_IAM

Note: please change Pem key name. Use your own pem key name in aimdek file.

After completed stack copy instance ip from cloudformation output and paste in inventory file
Now run ansbile file -->

ansible-playbook -i inventory ansible.yaml --private-key <your pem key name>
