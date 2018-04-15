# ansible-basics

The details on this page is from the book Ansible: Up and Running 

### Playbook
- In Ansible, a script is called a playbook.
- Ansible’s playbook syntax is built on top of YAML, which is a data format language that was designed to be easy for humans to read and write.
- In a way, YAML is to JSON what Markdown is to HTML.

### Comparison
Some configuration management systems that use agents, such as Chef and Puppet, are pull based by default. Agents installed on the servers periodically check in with a central service and pull down configuration information from the service. Making configuration management changes to servers goes something like this:

- You: make a change to a configuration management script.
- You: push the change up to a configuration management central service.
- Agent on server: wakes up after periodic timer fires.
- Agent on server: connects to configuration management central service.
- Agent on server: downloads new configuration management scripts.
- Agent on server: executes configuration management scripts locally that change server state.

In contrast, Ansible is push based by default. Making a change looks like this:

- You: make a change to a playbook.
- You: run the new playbook.
- Ansible: connects to servers and executes modules, which changes server state.

The push-based approach has a significant advantage: you control when the changes happen to the servers.
