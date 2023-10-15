# j-systembase

ansible role to have a functionnal host base, with useful tools, configurations and lib

## How to use it?

Use `tox` to generate the virtual env:

```bash
tox
source .tox/py3-ansible/bin/activate
```

Create instances, and connect to them:

```bash
molecule create
molecule login --host molecule-debian11
molecule login --host molecule-debian12
molecule login --host molecule-ubuntu
```

Install needed ansible collections (molecule will do it itself)

```bash
ansible-galaxy collection install -r requirements.yml
```

Use ansible/molecule on molecule hosts (check mode):

```bash
molecule converge
```

Destroy everything:

```bash
molecule destroy
```
