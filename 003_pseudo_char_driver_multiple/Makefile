obj-m := pcd_n.o
ARCH=arm
CROSS_COMPILE=arm-linux-gnueabihf-
KER_DIR =/home/aaron/workspace/ldd/source/linux_bbb_4.14/
HOST_KERN_DIR =/lib/modules/$(shell uname -r)/build/

all:
	make ARCH=$(ARCH) CROSS_COMPILE=$(CROSS_COMPILE) -C $(KER_DIR) M=$(PWD) modules
clean:
	make -C $(HOST_KERN_DIR) M=$(PWD) clean
help:
	make ARCH=$(ARCH) CROSS_COMPILE=$(CROSS_COMPILE) -C $(KER_DIR) M=$(PWD) help
host:
	make -C $(HOST_KERN_DIR) M=$(PWD) modules

