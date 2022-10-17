# PYNQ_zcu106

## Petalinux installation

* Download Petalinux installer from Xilinx website
`sudo chmod 777 ./Downloads/<installer>.run`
`mkdir -p /tools/Xilinx/PetaLinux/<version>`
`sudo chmod -R 755 /tools/Xilinx/PetaLinux/<version>/`
`sudo chown -R <user>:<user> /tools/Xilinx/PetaLinux/<version>/`
`cd Downloads`
`./<installer>.run /tools/Xilinx/PetaLinux/<version>/`

* [Hackster Guide](https://www.hackster.io/whitney-knitter/installing-vivado-vitis-petalinux-2021-2-on-ubuntu-18-04-0d0fdf)
* [Xilinx Guide](https://docs.xilinx.com/r/en-US/ug1144-petalinux-tools-reference-guide/Installing-the-PetaLinux-Tool)

## PYNQ Setup
* Follow this [guide](https://pynq.readthedocs.io/en/latest/pynq_sd_card.html#pynq-sd-card).
* When running `<PYNQ repository>/sdbuild/scripts/setup_host.sh` not in Ubunto 18.04 LTS some packages may not install. It may be necessary to install qemu and crosstool-ng manually (by using the commands in the script). Maybe the script can be used by changing some premissions. You might need to install [ncurses](https://www.cyberciti.biz/faq/linux-install-ncurses-library-headers-on-debian-ubuntu-centos-fedora/) separetly.
* Create XSA file for ZCU106 by following this [guide](https://discuss.pynq.io/t/tutorial-creating-a-hardware-design-for-pynq/145).