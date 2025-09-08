## Requirements
. mimalloc (optional)

## How to Install
. Place `tmpfs-overlay` in `/bin`

. Make the program executable

```
sudo chmod 755 /bin/tmpfs-overlay
```

. Add this section to `rc.local`

```
# TMPFS Overlay
if [ -x /bin/tmpfs-overlay ]; then
    ( sleep 0.1; setsid nohup /bin/tmpfs-overlay >/dev/null 2>&1 ) &
fi
```

. Restart system
