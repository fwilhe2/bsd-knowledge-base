# bsd-knowledge-base

## FreeBSD

https://stackoverflow.com/questions/49656395/how-to-boot-freebsd-image-under-qemu

```
wget https://download.freebsd.org/ftp/releases/VM-IMAGES/14.0-RELEASE/amd64/Latest/FreeBSD-14.0-RELEASE-amd64.raw.xz
xz -d FreeBSD-14.0-RELEASE-amd64.raw.xz
qemu-system-x86_64 -drive file=FreeBSD-14.0-RELEASE-amd64.raw,format=raw -enable-kvm
```

## NetBSD

```
qemu-system-x86_64 -drive file=netbsd.img,format=raw -cdrom Downloads/boot.iso -boot d
qemu-system-x86_64 -drive file=netbsd.img,format=raw -net nic -net user,hostfwd=tcp::2222-:22
```

http://netbsd.org/docs/guide/en/chap-boot.html#chap-boot-ssh
