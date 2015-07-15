# tw-ha
Deployment of HA web application using vagrant and ansible.

The envoronment consists of three Ansible roles:

"web" - A web role for hosting static assets using nginx.

"app" - An application role using jetty to host a .war file

"lb"  - A simple loadbalancer using haproxy to forward to the other tiers

There are three environments:

devenv - A development / training environment where all three roles are deployed to a single vm

single-instance - an initial production deployment with a single vm per role

multi-instance - a demonstration of a scale-out environment with multiple vms per role

quick start:

git clone https://github.com/stephenjirvine/tw-ha.git

cd tw-ha/vagrant/devenv/
vagrant up
