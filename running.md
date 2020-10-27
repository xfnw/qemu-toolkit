# normal running of the vm

## to start it

```bash
qemu-system-x86_64 -m 512 -nic user -nographic -hda image.qcow2
```

if you wish to daemonize without using `-daemonize` lmao,
and its complaining about suspending
stuff or something, put `</dev/null` at the end

## what if you want a port to be forwarded to the host???

in the `-nic` section, you can add
`hostfwd=tcp::<hostport>-:<vmport>` blocks after user, seperated
by commas


