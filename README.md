Ansible is an open source IT automation engine that automates provisioning, configuration management, application deployment, orchestration and many other IT processes. It is free to use, and the project benefits from the experience and intelligence of its thousands of contributors.

Ansible is agentless in nature, which means you don't need install any software on the manage nodes.

For automating Linux and Windows, Ansible connects to managed nodes and pushes out small programs—called Ansible modules—to them. These programs are written to be resource models of the desired state of the system. Ansible then executes these modules (over SSH by default), and removes them when finished. These modules are designed to be idempotent when possible, so that they only make changes to a system when necessary.

For automating network devices and other IT appliances where modules cannot be executed, Ansible runs on the control node. Since Ansible is agentless, it can still communicate with devices without requiring an application or service to be installed on the managed node.

Installing Ansible
------------------
Ansible is an agentless automation tool that you install on a single host (referred to as the control node).

From the control node, Ansible can manage an entire fleet of machines and other devices (referred to as managed nodes) remotely with SSH, Powershell remoting, and numerous other transports, all from a simple command-line interface with no databases or daemons required.



sudo apt install python3-pip

 sudo apt install ansible

Confirming your installation
You can test that Ansible is installed correctly by checking the version:

ansible --version
The version displayed by this command is for the associated ansible-core package that has been installed.

To check the version of the ansible package that has been installed:

ansible-community --version

