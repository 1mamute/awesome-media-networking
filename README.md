# Awesome Media Networking
[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

> A walkthrough over all things related to media networking.


## Contents
- [Awesome Media Networking](#awesome-media-networking)
  - [Contents](#contents)
  - [Codecs](#codecs)
    - [Lossless](#lossless)
      - [JPEG XS](#jpeg-xs)
    - [Lossy](#lossy)
    - [Transport Streams](#transport-streams)
      - [CBR](#cbr)
      - [Piecewise VBR](#piecewise-vbr)
      - [Non-piecewise VBR:](#non-piecewise-vbr)
  - [High Bit Rate Media Transport (HBRMT)](#high-bit-rate-media-transport-hbrmt)
  - [Standards](#standards)
    - [SMTPE ST 2022](#smtpe-st-2022)
    - [SMPTE ST 2110](#smpte-st-2110)
  - [Streaming](#streaming)
  - [Video Rendering](#video-rendering)
  - [IPMX](#ipmx)
  - [SAP](#sap)
  - [IEEE 1588v2](#ieee-1588v2)
  - [PTP \& PTPv2](#ptp--ptpv2)
  - [NMOS](#nmos)
  - [Network Analysis](#network-analysis)
  - [Audio Over IP / Audio Over Ethernet](#audio-over-ip--audio-over-ethernet)
  - [Audio Over Thread](#audio-over-thread)
  - [HDBaseT / Audio Over Cat](#hdbaset--audio-over-cat)
  - [AES67](#aes67)
  - [Dante](#dante)
  - [mDNS](#mdns)
  - [Ravenna](#ravenna)
  - [CobraNet](#cobranet)
  - [Tools](#tools)
  - [Resources](#resources)
    - [Groups](#groups)
    - [Books](#books)
    - [Papers](#papers)
    - [Articles](#articles)
    - [Newsletters](#newsletters)
    - [Journals](#journals)
    - [Blogs](#blogs)
    - [Podcasts](#podcasts)
    - [YouTube Channels](#youtube-channels)
    - [Events](#events)
  - [Miscellaneous](#miscellaneous)
  - [Related Lists](#related-lists)
  - [Contributing](#contributing)

## Codecs
### Lossless
#### JPEG XS
- [JPEGXS](https://jpeg.org/jpegxs/) ([Specification](https://ds.jpeg.org/whitepapers/jpeg-xs-whitepaper.pdf)) - The JPEG XS (ISO/IEC 21122) standard specifies a compression technology with an end-to-end latency of a few lines, at a low implementation complexity.
- [Introduction to the New JPEG XS Standard for Low-Latency, Visually Lossless Streaming in HD, 4K, and 8K](https://www.nvidia.com/en-us/on-demand/session/gtcspring21-s31734/) by Jean-Baptiste Lorent.
- FFmpeg - A cross-platform solution to record, convert and stream audio and video. Supports SMPTE ST 2110.

### Lossy

### Transport Streams
#### CBR
#### Piecewise VBR
A piecewise constant VBR transport stream can only vary at the PCRs of the program under consideration per ISO/IEC 13818-1:2007 § 2.4.2.2.
#### Non-piecewise VBR:
A non-piecewise constant VBR transport stream has no predictable time base to reconstruct the signal if the inter-packet timing is altered in transit through the network.
## High Bit Rate Media Transport (HBRMT)
> Formerly known as High Bit Rate Audio Video Over IP (HBRAV-IP)

Standard for data encapsulation and forward error correction (FEC) of high bit rate contribution oriented video/audio feed services, up to 3 Gbit/s over Ethernet networks. HBRMT is published as parts 5 and 6 of SMPTE 2022 by the [SMPTE 32NF networking technology committee](https://web.archive.org/web/20110125153532/http://www.videoservicesforum.org/SMPTE_32NF_Tech_Com.shtml). HBRMT supports both SDI uncompressed and JPEG 2000 compressed video and audio formats.

## Standards
### SMTPE ST 2022
The SMPTE ST 2022 suite of standards provides a reliable way of using IP to transmit signals that were traditionally sent over serial interfaces.

> To read more about every part of the SMPTE ST 2022 standard, head to [standards/SMPTE-ST-2022.md](standards/SMPTE-ST-2022.md)

- [smpte2110-analyzer](https://github.com/ebu/smpte2110-analyzer): Analyzer to inspect network packets generated by the SMPTE ST 2110 specification.

### SMPTE ST 2110
The SMPTE ST 2110 suite of standards specifies the carriage, synchronization, and description of separate elementary essence streams over IP for real-time media applications.

> To read more about every part of the SMPTE ST 2110 standard, head to [standards/SMPTE-ST-2110.md](standards/SMPTE-ST-2110.md)

- [JT-NM TR1001-1 "System Environment and Device Behaviors for ST 2110 Media Nodes in Engineered Networks"](https://static.jt-nm.org/documents/JT-NM_TR-1001-1_2020_v1.1.pdf): Technical Recommendation paper from JT-NM with a "goal to enable the creation of network environments where an end-user can take delivery of (recommended) equipment, connect it to their network, and configure it for use, with a minimum amount of human interaction."

## Streaming
- [NVIDIA® Rivermax®](https://developer.nvidia.com/networking/rivermax): GPU-accelerated media and data streaming IP-based solution. [Tools, Apps & Code Samples](https://github.com/NVIDIA/Rivermax)

## Video Rendering
- [Viz Engine](https://www.vizrt.com/products/viz-engine/): SMPTE ST 2110 And NMOS compatible Real Time Video Renderer

## IPMX
## SAP
## IEEE 1588v2
## PTP & PTPv2
## NMOS
Overview: https://www.amwa.tv/nmos-overview  
Specifications: https://specs.amwa.tv/nmos/
- [Pebble Control Free](https://www.pebble.tv/control-free/about/): Self-contained, scalable and easy to configure IP connection manager.
- [nmos-cpp](https://github.com/sony/nmos-cpp): Sony's NMOS Registry and Node Implementation in C++.
- [nmos-js](https://github.com/sony/nmos-js): Sony's NMOS Client Implementation in Javascript.
- [BBC's NMOS Authorisation Server Implementation](https://github.com/bbc/nmos-auth-server): A Flask-based implementation of an OAuth2 Authorisation Server based on [AMWA NMOS BCP-003-02](https://amwa-tv.github.io/nmos-api-security/best-practice-authorisation.html) using [RFC 6749](https://tools.ietf.org/html/rfc6749).
- [Ledger](https://github.com/Streampunk/ledger): Node.js Javascript implementation of the NMOS discovery and registration APIs.
- [Easy-NMOS Docker Compose Solution](https://github.com/rhastie/easy-nmos): Easy NMOS setup using Docker compose
- [NMOS-TESTING](https://specs.amwa.tv/nmos-testing/): Testing tool for the AMWA NMOS Specifications ([GitHub Repo](https://github.com/AMWA-TV/nmos-testing))
- [The Business Benefits of DNS-SD for NMOS](http://static.amwa.tv/business-benefits-of-nmos-plus-dns-sd.pdf): Why DNS Service Discovery in an NMOS environment?
- [NMOS Web Router](https://github.com/bbc/nmos-web-router): A web based application for connecting multicast RTP Senders and Receivers using AMWA NMOS IS-04 and IS-05. 

## RTMFP
- https://github.com/zenomt/rtmfp-cpp
## Network Analysis
- wireshark

## Audio Over IP / Audio Over Ethernet
Specifications:

## Audio Over Thread
Specifications:

## HDBaseT / Audio Over Cat

## AES67
Specifications:

## Dante
Specifications:

## mDNS
- RFC 6762 - mDNS - http://tools.ietf.org/html/rfc6762
- RFC 6763 - DNS Based Service Discovery (DNS-SD) - http://tools.ietf.org/html/rfc6763
- http://www.tcpipguide.com/free/t_DNSMessageHeaderandQuestionSectionFormat.htm
- https://github.com/mdns-js/node-mdns-js
- http://en.wikipedia.org/wiki/Multicast_DNS
- http://en.wikipedia.org/wiki/Zero_configuration_networking#Service_discovery
## Ravenna
Specifications:

## CobraNet
Specifications:

## Tools

- [Media Network Manager Cloud (MnMs)](https://github.com/nicolassturmel/media-network-manager-cloud)


## Resources

### Groups
- AIMS
- AMWA
- SMPTE
- VSF
- AES
- AVIXA
- AVNU
- [JT-NM](https://www.jt-nm.org/)
  
### Books

### Papers
- https://aimsalliance.org/wp-content/uploads/2019/04/AES67-SMPTE-ST-2110-Commonalities-and-Constraints-Updated-April-2019.pdf
### Articles
- https://www.commercialintegrator.com/networks/information_technology/av-as-a-service-requires-you-to-speak-its-language/
- https://www.avnetwork.com/news/how-to-achieve-global-interoperability
- https://www.avnetwork.com/news/dirty-hands-and-ipmx
- https://www.avnetwork.com/news/ipmxs-soft-spot
- https://www.avnetwork.com/news/for-ipmx-its-about-time
- https://www.avnetwork.com/news/ipmxs-strength-is-its-interoperability
- https://www.avnetwork.com/news/ipmx-media-experience-nirvana
- https://www.avnetwork.com/features/ipmx-the-next-great-av-standard
- https://www.avnetwork.com/news/deep-dive-do-you-know-the-difference-between-ipmx-and-smpte-st-2110-and-aes67
- https://medium.com/canal-tech/why-we-use-a-multicast-ip-network-for-live-content-production-697a57b86766


### Newsletters
- https://www.avnetwork.com/
- https://www.tvtechnology.com/

### Journals

### Blogs
- https://medium.com/canal-tech
- 
### Podcasts
- https://higheredav.com/060-james-king-audio-visual-specialist-at-stockton-university/
- https://higheredav.com/024-10-minute-take-dante-av-by-audinate/
- 
### YouTube Channels

### Events
- InfoComm
- 
## Miscellaneous
- [Network Engineering Stack Exchange](https://networkengineering.stackexchange.com/)
- [Server Fault](https://serverfault.com/) - A question and answer site for system and network administrators.
- [/r/Networking](https://www.reddit.com/r/networking/) - Reddit group for networking.

## Related Lists

- [Awesome Broadcasting](https://github.com/ebu/awesome-broadcasting)
- [Awesome Networking](https://github.com/facyber/awesome-networking)
- [Awesome Music](https://github.com/noteflakes/awesome-music)
- [Awesome Real Time Communication](https://github.com/rtckit/awesome-rtc)
- [Awesome SNMP](https://github.com/eozer/awesome-snmp)
- [Awesome Software Defined Network](https://github.com/sdnds-tw/awesome-sdn)
- [Awesome Linux Audio](https://github.com/nodiscc/awesome-linuxaudio)
- [Awesome Networking Automation](https://github.com/networktocode/awesome-network-automation)

## Contributing

Contributions welcome! Read the [contribution guidelines](contributing.md) first.
