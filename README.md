### How to run CSI Tests

https://github.com/cniackz/public/wiki/How-to-run-CSI-Tests

### RedHat Case:

* https://rhcert.connect.redhat.com/#/cases/03629102
* https://rhcert.connect.redhat.com/#/cases/04212901

# directpvcertification
DirectPV Certification Files

### Result progression:

* When we started using crc:

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

* With real OpenShift Cluster:

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

error running options: 4 fail, 33 pass, 217 skip (7m0s)error: 4 fail, 33 pass, 217 skip (7m0s)
```

* With real OpenShift Cluster with at least 3 control planes:

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

error running options: 5 fail, 36 pass, 213 skip (8m17s)error: 5 fail, 36 pass, 213 skip (8m17s)

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

* Mon Apr 8 2024 with below:

```
parameters:
  csi.storage.k8s.io/fstype: "xfs"
```

```
Suite run returned error: 1 fail, 40 pass, 213 skip (6m27s)

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

error running options: 1 fail, 40 pass, 213 skip (6m27s)error: 1 fail, 40 pass, 213 skip (6m27s)
```

* Thu Jul 31 2025 with below:

```
Suite run returned error: 1 fail, 41 pass, 232 skip (8m8s)
error running options: 1 fail, 41 pass, 232 skip (8m8s)error: 1 fail, 41 pass, 232 skip (8m8s)
```













