# PYNQ ZCU106

# Xilinx Tools Instalation
* Use Ubuntu 18.04 LTS.
* With Xilinx Unified Installer, install Vitis, Vitis HLS, Vivado, DocNav and for SOCs anything related with ZYNQ-7000, Ultrascale+ MPSoC and Artix7.
* Check if `libtinfo5 libncurses5-dev libncursesw5-dev libncurses5 libtinfo-dev` package is installed. If it is not, install it before proceeding with Xilinx installation otherwise it will freeze in the end.
Found this solution in this [forum](https://support.xilinx.com/s/question/0D52E00006hpRxQSAU/vivado-20202-installation-stuck-at-generating-installed-device-list-on-ubuntu-2004lts?language=en_US).

	## Petalinux installation

* Download Petalinux installer with Xilinx Unified Installer 
* Run installer at `<petalinux-path>/<installer>.run`
* Setup TFTP server, this [tutorial](https://www.instructables.com/Setting-Up-TFTP-Server-for-PetaLinux/) worked. 

* [Hackster Guide](https://www.hackster.io/whitney-knitter/installing-vivado-vitis-petalinux-2021-2-on-ubuntu-18-04-0d0fdf)
* [Xilinx Guide](https://docs.xilinx.com/r/en-US/ug1144-petalinux-tools-reference-guide/Installing-the-PetaLinux-Tool)

	## PYNQ Setup
* Follow this [guide](https://pynq.readthedocs.io/en/latest/pynq_sd_card.html#pynq-sd-card).
* Repository can't be on mounted device, run it in a home subdirectory.
* When running `<PYNQ repository>/sdbuild/scripts/setup_host.sh`. It may be necessary to install qemu and crosstool-ng manually (by using the commands in the script). Maybe the script can be used by changing some premissions. You might need to install [ncurses](https://www.cyberciti.biz/faq/linux-install-ncurses-library-headers-on-debian-ubuntu-centos-fedora/) separetly.
* Get ZCU106 BSP file [here](https://xilinx-wiki.atlassian.net/wiki/spaces/A/pages/444006775/Zynq+UltraScale+MPSoC).
* Get XSA from BSP by running `petalinux-create -t project -s <path-to-bsp>`. Enter the new directory created. There should be an hardware folder where you will find a Vivado project, open the project and export hardware.
* After image is created use this guide (it is not specific to ZCU106 but can help): [zcu104 pynq setup](https://pynq.readthedocs.io/en/latest/getting_started/zcu104_setup.html)

* **Might be useful for other applications:**
* To create XSA file for ZCU106 by following this [guide](https://discuss.pynq.io/t/tutorial-creating-a-hardware-design-for-pynq/145).
* https://discuss.pynq.io/t/pynq-3-0-fails-quemu-version-check/4776
* https://www.hackster.io/whitney-knitter/installing-vivado-vitis-petalinux-2021-2-on-ubuntu-18-04-0d0fdf


## FPGA Setup
* xdc file availabe [here](https://www.xilinx.com/products/boards-and-kits/zcu106.html#documentation) in Documentation - Board Files