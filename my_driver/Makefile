# If we make if obj-y here, then it wont give the .ko file.
obj-m += hello.o

KERNELDIR ?= /lib/modules/$(shell uname -r)/build

all : modules

# the below command requires tab spacing otherwise it will give "missing separator issue"
modules clean : 
	$(MAKE) -C $(KERNELDIR) M=$(shell pwd) $@ 
