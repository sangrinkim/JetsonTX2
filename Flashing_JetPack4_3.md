# Jetson TX2 Flashing (JetPack 4.3)

Test device: AN310(Aetina Jetson TX2 board)
Host OS: Ubuntu 18.04.3 LTS

### Steps:

	1. Install Ubuntu 18.04
	
    2. download AN310 patch files
    > [Aetina](https://www.aetina.com/products-detail.php?i=252)
	
    3. download 
    > [Jetpack sdkmanager 4.3](https://developer.nvidia.com/embedded/jetpack-archive)
    > nvidia sdk manager [documents](https://docs.nvidia.com/sdk-manager/download-run-sdkm/index.html)
	
    4. Install utility and python 2.7
    > `sudo apt install bzip2=1.0.6-8.1 libbz2-1.0=1.0.6-8.1`

	5. install NVIDIA sdkmanager
    > `sudo apt install ./sdkmanager_[version]_amd64.deb`

	6. Login

	7. Download Jetson TX2 File System and OS and Component

	8. Logout >>  select OFFLINE from local folder tab >> START

	9. Wait until make Jetson OS Image

	10. copy AN310 patch file to nvidia_sdk folder

	11. extract patch file
    > `sudo tar -zxvf R32_3_1_TX2_N310_1.tar.gz`

	12. update path in setup.sh file

	13. execute setup.sh
    > `./setup.sh`
    > you can see "DONE" on terminal

	14. sudo ./flash.sh jetson-tx2 mmcblk0p1

	15. reboot Jetson TX2 after install

	16. install Jetson SDK components via LAN(need Jetson TX2 IP address)

	17. Check JetPack Version
    > `cat /etc/nv_tegra_release`
	


### Jetson TX2 default account
user / password: nvidia / nvidia
