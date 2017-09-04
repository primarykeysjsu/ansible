Building a simple Apache2 Webserver stack and deploying Application using Ansible Playbooks.
-------------------------------------------

These playbooks require Ansible

These playbooks are meant to be a reference and starter's guide to building
Ansible Playbooks. These playbooks were tested on Ubuntu EC2 Amazon Instance.

This apache2 installation can be on a single node or multiple nodes. The inventory file
'hosts' defines the nodes in which the stacks should be configured.

        [awsServers]

Here the webserver would be configured on the awsServers. The stack can be deployed using the following
command:

        ansible-playbook -s site.yml (-s allows ansible to perform sudo)

Once done, you can check the results by browsing to ec2 instance created.
You should see a simple test page with a custom HTML

Sample Hosts File
[awsServers]
ec2-54-69-142-58.us-west-2.compute.amazonaws.com ansible_ssh_private_key_file=/Users/rajisunder/authorized_keys/sunderaws.pem remote_user=ubuntu
