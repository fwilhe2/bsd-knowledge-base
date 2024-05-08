# bsd-knowledge-base

## FreeBSD

https://stackoverflow.com/questions/49656395/how-to-boot-freebsd-image-under-qemu

```bash
wget https://download.freebsd.org/ftp/releases/VM-IMAGES/14.0-RELEASE/amd64/Latest/FreeBSD-14.0-RELEASE-amd64.raw.xz
xz -d FreeBSD-14.0-RELEASE-amd64.raw.xz
qemu-img resize FreeBSD-14.0-RELEASE-amd64.raw 50G
qemu-system-x86_64 -drive file=FreeBSD-14.0-RELEASE-amd64.raw,format=raw -enable-kvm
```

Inside the VM:

```bash
pkg update
pkg install curl bash git vim

adduser
```

## NetBSD

```bash
qemu-system-x86_64 -drive file=netbsd.img,format=raw -cdrom Downloads/boot.iso -boot d
qemu-system-x86_64 -drive file=netbsd.img,format=raw -net nic -net user,hostfwd=tcp::2222-:22
```

http://netbsd.org/docs/guide/en/chap-boot.html#chap-boot-ssh

## Links

https://rubenerd.com/basics-of-freebsd-services/
