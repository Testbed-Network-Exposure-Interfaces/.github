# Testbed for Testing Network Exposure Interfaces

This organization hosts the code, documentation and overall contributions for the dissertation **"Testbed for Testing Network Exposure Interfaces"**, submitted to the **University of Aveiro** in fulfillment of the requirements for the degree of Master in Informatics Engineering.

## Repositories

| Repository | Description |
|---|---|
| [tmf-services](https://github.com/Testbed-Network-Exposure-Interfaces/tmf-services) | TM Forum (TMF) Open API services for the testbed. |
| [network-observability](https://github.com/Testbed-Network-Exposure-Interfaces/network-observability) | Network observability tooling for the testbed: a per-slice monitoring Helm chart deployed through Argo CD/OpenSlice (slice poller, ICMP prober and Grafana dashboards), a Prometheus throughput exporter written in Go that counts per-IP/MAC bytes and packets, and a packet-mirroring setup that streams captured traffic between VMs. |
| [NEF_emulator](https://github.com/Testbed-Network-Exposure-Interfaces/NEF_emulator) | Fork of [ATNoG/NEF_emulator](https://github.com/ATNoG/NEF_emulator): a configurable, emulated environment that provides 3GPP Network Exposure Function (NEF) APIs. In this dissertation, it was integrated with the new Slice Manager API, which enforces QoS through the Slice Manager, and gained an implementation of the Analytics Exposure API. That API is backed by Prometheus and the monitoring setup in [network-observability](https://github.com/Testbed-Network-Exposure-Interfaces/network-observability). |
| [gsma-open-gw-apis](https://github.com/Testbed-Network-Exposure-Interfaces/gsma-open-gw-apis) | Fork of [ATNoG/gsma-open-gw-apis](https://github.com/ATNoG/gsma-open-gw-apis): a GSMA Open Gateway / CAMARA API gateway built on the NEF (e.g. Quality on Demand, Location, SMS OTP). In this dissertation, the Application Profiles and Connectivity Insights Subscriptions APIs were implemented. |
| [VehicleDetectionPoC](https://github.com/Testbed-Network-Exposure-Interfaces/VehicleDetectionPoC) | Proof-of-concept Vehicle Crash Detection network application that exercises the testbed's NEF and CAMARA APIs. A computer-vision model detects crashes in a camera UE's video feed, and the app then sends SMS alerts to pedestrian UEs geofenced near the incident. It also manages the camera's QoS profile and monitors its SLA. Ships with a backend, a React frontend, a video streaming component and Helm charts. |

## Author

**Miguel Belchior Figueiredo**: [miguel.belchior@ua.pt](mailto:miguel.belchior@ua.pt) · [@Migas77](https://github.com/Migas77)

Supervised by *Dr. Diogo Nuno Pereira Gomes*, *Associate Professor in the Department of Electronics, Telecommunications and Informatics at the University of Aveiro*, and *Dr. Rui Luís Andrade Aguiar*, *Chair Professor in the Department of Electronics, Telecommunications and Informatics at the University of Aveiro*.
