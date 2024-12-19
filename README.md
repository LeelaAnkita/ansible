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

Confirming your installation
----------------------------
You can test that Ansible is installed correctly by checking the version:

ansible --version
The version displayed by this command is for the associated ansible-core package that has been installed.

To check the version of the ansible package that has been installed:

ansible-community --version

Ansible Roles
An Ansible role is a reusable, self-contained unit of automation that is used to organize and manage tasks, variables, files, templates, and handlers in a structured way.

Roles help to encapsulate and modularize the logic and configuration needed to manage a particular system or application component.

This modular approach promotes reusability, maintainability, and consistency across different playbooks and environments.

Key Components of an Ansible Role
Tasks
The main list of actions that the role performs.

Handlers
Tasks that are triggered by changes in other tasks, typically used for actions like restarting services.

Files
Static files that need to be transferred to managed hosts.

Templates
Jinja2 templates that can be rendered and transferred to managed hosts.

Vars
Variables that are used within the role.

Defaults
Default variables for the role, which can be overridden.

Meta
Metadata about the role, including dependencies on other roles.

Library
Custom modules or plugins used within the role.

Module_defaults
Default module parameters for the role.

Lookup_plugins
Custom lookup plugins for the role.

Directory Structure of an Ansible Role
An Ansible role follows a specific directory structure:

<role_name>/
  ├── defaults/
  │   └── main.yml
  ├── files/
  ├── handlers/
  │   └── main.yml
  ├── meta/
  │   └── main.yml
  ├── tasks/
  │   └── main.yml
  ├── templates/
  ├── vars/
      └── main.yml
Why Use Ansible Roles?
Modularity
Roles allow you to break down complex playbooks into smaller, reusable components. Each role handles a specific part of the configuration or setup.

Reusability
Once created, roles can be reused across different playbooks and projects. This saves time and effort in writing redundant code.

Maintainability
By organizing related tasks into roles, it becomes easier to manage and maintain the code. Changes can be made in one place and applied consistently wherever the role is used.

Readability
Roles make playbooks cleaner and easier to read by abstracting away the details into logically named roles.

Collaboration
Roles facilitate collaboration among team members by allowing them to work on different parts of the infrastructure independently.

Consistency
Using roles ensures that the same setup and configuration procedures are applied uniformly across multiple environments, reducing the risk of configuration drift.
