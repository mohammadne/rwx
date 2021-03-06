# Virtual Machine

> virtual machine manager + kvm + QMUE will give you the hypervisor type 1
>
> the virtualBox gives you hypervisor type 2

1. install `virtual machine manager`

    ``` bash
    sudo dnf install virt-manager
    ```

2. start `libvirtd`

    ``` bash
    sudo systemctl start libvirtd
    sudo systemctl enable libvirtd

    sudo systemctl status libvirtd

    sudo usermod -a -G libvirt $(whoami)
    ```

3. download an ISO and install virtual machine

4. install necessary tools on vm

    ``` bash
    sudo apt update

    # install ssh server on VM
    sudo apt install openssh-server
    sudo systemctl enable ssh
    sudo systemctl start ssh

    # copy the inet ip
    ip address show
    ```

5. connect to the VM via ssh

    ``` bash
    ssh <server-username>@<ip-address>
    ```
