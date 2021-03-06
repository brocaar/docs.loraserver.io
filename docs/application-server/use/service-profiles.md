---
description: Manage Service Profile, defining the features that organizations are allowed to use on a connected network-server.
---

# Service profiles

The Service Profile can be seen as the "contract" between an user and the
network. It describes the features that are enabled for the user(s) of the
Service Profile and the rate of messages that can be sent over the network.

When creating a Service Profile, ChirpStack Application Server will create the actual
profile on the selected Network Server, and will keep a reference record
so it knows to which organization it belongs.

## Fields / options

The following fields are described by the
[LoRaWAN<sup>&reg;</sup> Backend Interfaces specification](https://www.lora-alliance.org/lorawan-for-developers).
Fields marked with an **X** are implemented by ChirpStack Application Server.

- [ ] **ULRate** Token bucket filling rate, including ACKs (packet/h)
- [ ] **ULBucketSize** Token bucket burst size
- [ ] **ULRatePolicy** Drop or mark when exceeding ULRate
- [ ] **DLRate** Token bucket filling rate, including ACKs (packet/h)
- [ ] **DLBucketSize** Token bucket burst size
- [ ] **DLRatePolicy** Drop or mark when exceeding DLRate
- [X] **AddGWMetadata** GW metadata (RSSI, SNR, GW geoloc., etc.) are added to the packet sent to AS
- [X] **DevStatusReqFreq** Frequency to initiate an End-Device status request (request/day)
- [X] **ReportDevStatusBattery** Report End-Device battery level to AS
- [X] **ReportDevStatusmargin** Report End-Device margin to AS
- [X] **DRMin** Minimum allowed data rate. Used for ADR.
- [X] **DRmax** Maximum allowed data rate. Used for ADR.
- [ ] **ChannelMask** Channel mask. sNS does not have to obey (i.e., informative).
- [ ] **PRAllowed** Passive Roaming allowed
- [ ] **HRAllowed** Handover Roaming allowed
- [ ] **RAAllowed** Roaming Activation allowed
- [X] **NwkGeoLoc** Enable network geolocation service
- [ ] **TargetPER** Target Packet Error Rate
- [ ] **MinGWDiversity** Minimum number of receiving GWs (informative)
