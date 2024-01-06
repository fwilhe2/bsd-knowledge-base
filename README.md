# bsd-knowledge-base

## NetBSD

```
qemu-system-x86_64 -drive file=netbsd.img,format=raw -cdrom Downloads/boot.iso -boot d
qemu-system-x86_64 -drive file=netbsd.img,format=raw -net nic -net user,hostfwd=tcp::2222-:22
```

http://netbsd.org/docs/guide/en/chap-boot.html#chap-boot-ssh
