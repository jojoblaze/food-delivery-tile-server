
# Tile server

Tile server documentation at [https://maptiler-tileserver.readthedocs.io](https://maptiler-tileserver.readthedocs.io)

## Setup

In order to provide maps files on startup, a mount volume is needed.
Volume must be located at ``/persistent-volume`` path.


- dev machine -> create a folder to host ``persistent-volume`` data. For example: ``/home/user/.food-delivery-kind-volume``
- Kind cluster -> setup the cluster with an **extraMount** 

```
  extraMounts:
  - hostPath: /home/user/.food-delivery-kind-volume
    containerPath: /persistent-volume
```

in this way the tileserver can have access to maps files on developer machine through the volume located at ```/persistent-volume```


## Docker cheats


## Kind cheats

Get a console on pod container
```
kubectl exec -it map-tile-server-5cd7694b74-s6g6g -- /bin/bash
```
