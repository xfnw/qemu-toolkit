# creating a qemu vm

## create a virtual device/image

```bash
qemu-img create -f qcow2 image.qcow2 16G
```
- image.qcow2: file name for the image
- 16G: the maximum size it may take up, note
  that it will not take up that space while not filled.

## install an os

to boot with an install iso,
```bash
qemu-system-x86_64 -m 512 -nic user -nographic \
 -hda image.qcow2 -cdrom alpine-something.iso -boot d
```
- 512: the max amount of ram, in mb
- image.qcow2: the image from before
- alpine-something.iso: your install iso

this will boot up a vm with your install iso any then you
can install stuff, eg with `setup-alpine`




