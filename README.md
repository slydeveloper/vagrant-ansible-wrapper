Vagrant Ansible Wrapper
===========================================
Here is example how to run Ansible project on pre-installed Vagrant machine.

Goals
------
Run Ansible project without installing Ansible tool (i.e: Ansible does not support MS Windows). Ansible project is "mounted" to Vagrant machine. Example consists of two machines:

- `ansible` - machnie contains pre-installed Anaible tool and example Ansible project
- `host` - test machine where Ansible runs scripts agains

Requirements
------------
- Vagrant (tested on `2.0.1`)
- VirtualBox (tested on `5.2.6`)

Commands
--------
- Run Vagrant machines: `vagrant up`
- Ansible machine status: `vagrant status ansible`
- Host machine status: `vagrant status host`
- Stop Vagrant machines: `vagrant halt`
- Suspend Vagrant machines: `vagrant suspend`
- Destroy Vagrant machines: `vagrant destroy`

Usage
-----
- Run Vagrant machines: `vagrant up`
- Login to Vagrant ansible machine: `vagrant ssh ansible`
- Go to Ansible example project: `cd ansible-example`
- Eun Ansible command: `ansible all -i inventory -m ping -vv`
- Example response from host machine:
```
host | SUCCESS => {
    "changed": false,
    "ping": "pong"
}
```
