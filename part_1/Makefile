KERNEL_DIR=/home/pi/build

ARCH=arm
CROSS_COMPILE=arm-linux-gnueabihf-
export  ARCH  CROSS_COMPILE

obj-m := helloworld.o 

all:
	$(MAKE) -C $(KERNEL_DIR) M=$(CURDIR) modules

.PHONE:clean copy 

clean:
	$(MAKE) -C $(KERNEL_DIR) M=$(CURDIR) clean	
	sudo rm /home/ccb/nfs_workdir/*.ko

copy:
	sudo cp *.ko /home/ccb/nfs_workdir
