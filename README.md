# Ansible Collection - mansourka06.webapp

[Documentation for the collection](https://docs.ansible.com/collections.html)
# ansible-collection-webapp

## Description

- Ansible Collections are a way to package and distribute Ansible content, including playbooks, roles, modules, and plugins, in a versioned manner. 
- They allow you to share and consume reusable automation content across different Ansible projects and environments.


## Organisation of collections

1. **Structure of a Collection:**

An Ansible Collection typically consists of one or more roles, modules, plugins, and playbooks, organized into a specific directory structure. Collections are distributed as tarballs or Python wheels.

2. **Namespace and Naming Convention:**

Collections follow a naming convention based on a namespace. The namespace is used to organize and identify collections, preventing naming conflicts. Collections have names in the format: 

```yaml
namespace.collection_name
```

3. **Roles and Modules:**

Collections often contain roles and modules, which are reusable pieces of automation code. Roles encapsulate tasks and templates, while modules are single, reusable units of code that can be called directly from Ansible tasks.

4. **Galaxy and Automation Hub:**

- Ansible Collections are published and shared through [Ansible Galaxy](https://galaxy.ansible.com/) and [Automation Hub](https://cloud.redhat.com/ansible/automation-hub). 
- You can search for collections on these platforms and easily integrate them into your projects.

5. **Collection Installation:**

- Collections can be installed using the ***ansible-galaxy*** command. 
- For example, to install a collection ***named namespace.collection_name***, use:

```yaml
ansible-galaxy collection install namespace.collection_name
```

6. **Collection init:**

- Collections can be installed using the ***ansible-galaxy*** command. 
- For example, to install a collection ***named namespace.collection_name***, use:

```yaml
ansible-galaxy collection init namespace.collection_name
```

## Init submodules

run this commands to add our roles in the ansible collection (to do for each role):
```yaml
git submodule add  <role_url_repository> <role_name>
exemple: git submodule add https://github.com/mansourka06/ansible-role-nginx.git nginx

```

## build collection:
push all the changes to the collection repository.


## Create release pipeline for ansible-collection-webapp

We can create a pipeline to build a release of our collection when a new tags is created. For this: 
- Create the release pipeline in the path: .github/workflows
- add the [content](.github/workflows/release.yml) pipeline to the file. (example: .github/workflows/release.yml)


## Author
* [Mansour KA](http://mansourka.com)