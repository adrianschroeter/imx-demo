#
# Small cross architecture image build demo
#

To build this call the following commands to get the toolchain once:

```shell
 # git clone https://github.com/openSUSE/obs-build.git ~/obs-build

 # chmod 0666 /dev/kvm
   (KVM is required for kiwi builds as Building using chroot or container 
    env would fail, maybe damage your system and would not build right results)
```

Afterwards go into this directory and run the build using

```shell
 # ~/obs-build/pbuild --vm-disk-size 8192
```

The default preset expects a x86_64 build host and it will cross build
rpm package and resulting kiwi image for aarch64 architecture.

A build native on an aarch64 system is also supported via the "aarch64" preset:

```shell
 # ~/obs-build/pbuild --vm-disk-size 8192 --preset aarch64
```

