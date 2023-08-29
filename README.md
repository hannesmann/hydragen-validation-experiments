# hydragen-validation-experiments

Results from HydraGen validation experiments

## Lower boundary

This test determines the lower boundary for a request sent to the application emulator.
This is done by measuring the CPU time used to respond to a request with no stressors.

**Configurations**

- [config/old-main-branch/baseline.json](config/old-main-branch/baseline.json)
- [config/new-dev-branch/baseline.json](config/new-dev-branch/baseline.json)

| HydraGen v3.0.1 "processes": 1                                               | HydraGen dev branch "processes": 1                                          |
| ---------------------------------------------------------------------------- | --------------------------------------------------------------------------- |
| ![ctr p:1 old](stats/baseline/old-main-branch/svc:service-1%20ctr%20p:1.png) | ![ctr p:1 new](stats/baseline/new-dev-branch/svc:service-1%20ctr%20p:1.png) |

| HydraGen v3.0.1 "processes": 2                                               | HydraGen dev branch "processes": 2                                          |
| ---------------------------------------------------------------------------- | --------------------------------------------------------------------------- |
| ![ctr p:2 old](stats/baseline/old-main-branch/svc:service-1%20ctr%20p:2.png) | ![ctr p:2 new](stats/baseline/new-dev-branch/svc:service-1%20ctr%20p:2.png) |

| HydraGen v3.0.1 "processes": 3                                               | HydraGen dev branch "processes": 3                                          |
| ---------------------------------------------------------------------------- | --------------------------------------------------------------------------- |
| ![ctr p:3 old](stats/baseline/old-main-branch/svc:service-1%20ctr%20p:3.png) | ![ctr p:3 new](stats/baseline/new-dev-branch/svc:service-1%20ctr%20p:3.png) |

| HydraGen v3.0.1 "processes": 5                                               | HydraGen dev branch "processes": 5                                          |
| ---------------------------------------------------------------------------- | --------------------------------------------------------------------------- |
| ![ctr p:5 old](stats/baseline/old-main-branch/svc:service-1%20ctr%20p:5.png) | ![ctr p:5 new](stats/baseline/new-dev-branch/svc:service-1%20ctr%20p:5.png) |

## Bookinfo

This test attempts to recreate the [Bookinfo Application](https://istio.io/latest/docs/examples/bookinfo) from Istio. More specifically, this test determines if the new Go version of the application emulator (HydraGen dev branch) is able to accurately recreate the CPU complexity of the `reviews-v1` and `ratings` microservices.
