# build-test-linuxkernel-CI

This repository is Ansible blueprint for automating patching, compiling and  testing of the Linux kernel on qemu machine

## Roles
the project consists of three roles Patch, Compile, Test

### Patch
Patch is an ansible-playbook responsible for applying a patch file called "changes.patch" to the Linux kernel directory.

```
|-->files
   |
   |-- apply-patch.sh
   |-- changes.patch
   |-- linux-kernel ( directory)
|-->tasks
   |-- main.yml
```
`apply-patch.sh` is a bash script runs git command to apply the patch. <br>
`changes.pathc` is a patch file. <br>
`linux-kernel` is the linux kernel directory. <br>
`main.yml` is the ansible playbook. <br>

### Compile
Compile is an ansible-playbook responsible for compiling the Linux kernel on a remote machine.

```
|-->tasks
   |-- main.yml
```
`main.yml` is the ansbile-playbook 

## Test
The test is an empty role that you can modify based on your project requirements.
