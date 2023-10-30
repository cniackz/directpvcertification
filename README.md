# directpvcertification
DirectPV Certification Files

```
Storage Capabilities (guaranteed only on full CSI test suite with 0 fails)
==========================================================================
Driver short name:                         directpv
Driver name:                               directpv.min.io
Storage class:                             storageclass.yaml
Supported OpenShift / CSI features:
  Persistent volumes:                      true
  Raw block mode:                          false
  FSGroup:                                 true
  Executable files on a volume:            false
  Volume snapshots:                        false
  Volume cloning:                          false
  Use volume from multiple pods on a node: false
  ReadWriteMany access mode:               false
  Volume expansion for controller:         false
  Volume expansion for node:               true
  Volume limits:                           false
  Volume can run on single node:           true
  Topology:                                true
Supported OpenShift Virtualization features:
  Raw block VM disks:                      false
  Live migration:                          false
  VM snapshots:                            false
  Storage-assisted cloning:                false

error: 37 fail, 1 pass, 213 skip (30m25s)
```

### With exec as true, results are:

```sh
Writing JUnit report to /data/results/junit_e2e__20231030-220001.xml

Suite run returned error: 39 fail, 1 pass, 211 skip (40m33s)
Shutting down SimultaneousPodIPController
SimultaneousPodIPController shut down

Storage Capabilities (guaranteed only on full CSI test suite with 0 fails)
==========================================================================
Driver short name:                         directpv
Driver name:                               directpv.min.io
Storage class:                             storageclass.yaml
Supported OpenShift / CSI features:
  Persistent volumes:                      true
  Raw block mode:                          false
  FSGroup:                                 true
  Executable files on a volume:            true
  Volume snapshots:                        false
  Volume cloning:                          false
  Use volume from multiple pods on a node: false
  ReadWriteMany access mode:               false
  Volume expansion for controller:         false
  Volume expansion for node:               true
  Volume limits:                           false
  Volume can run on single node:           true
  Topology:                                true
Supported OpenShift Virtualization features:
  Raw block VM disks:                      false
  Live migration:                          false
  VM snapshots:                            false
  Storage-assisted cloning:                false

error: 39 fail, 1 pass, 211 skip (40m33s)
```
