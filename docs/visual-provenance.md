# Visual sources and presentation notes

[Back to the project](../README.md)

The published visuals come from the project's original report and presentation. PDF screenshots were extracted from embedded images. Demo stills were decoded from the video embedded in the presentation. Images were cropped at native resolution and saved as losslessly optimized PNGs. No metrics, rule fields, dates, addresses, alert descriptions, or statuses were changed.

## Materials reviewed

- `RapportFinal_Erraouidate_ISMAIL_PFA_Pfsense.pdf`: 56 PDF pages, including front matter. Figure references below use PDF page numbers, with the cover counted as page 1.
- `finalPresentation.pptx`: 19 slides. Slide 18 contains an approximately 110.34-second demo video with a native frame size of 3840 × 2160.

The report identifies academic year **2025–2026**. The presentation identifies **2026–2027**, a defense date of **September 29, 2026**, and a demo recorded with September 28 visible on screen. The source-year discrepancy is preserved here rather than resolved by assumption. It does not affect the technical evidence.

The report describes earlier configuration and test stages; the presentation adds a later WAN-side scan and an explicit view of Suricata's operating mode. The final README uses both sources where one supplies evidence the other does not.

## Published image inventory

Crop coordinates are `(left, top, right, bottom)` in the native extracted image or decoded video frame. A full image has no crop. Dimensions describe the published PNG.

| Asset | Source | Published size | Crop | Why it was selected |
| --- | --- | --- | --- | --- |
| [Original topology](../assets/architecture/original-topology.png) | Report figure 2.2, PDF p22 | 1102 × 1078 | Full image | Documents the original design and zone addresses |
| [Ubuntu Grafana](../assets/monitoring/ubuntu-grafana.png) | Figure 5.1, PDF p47 | 1615 × 598 | Full image | Clearest overview of the working monitoring interface after DMZ migration |
| [pfSense Grafana](../assets/monitoring/pfsense-grafana.png) | Figure 5.2, PDF p47 | 1877 × 482 | Full image | Shows the firewall's status, uptime, latency, and packet-loss panels |
| [Zabbix Latest Data](../assets/monitoring/zabbix-latest-data.png) | Figure 4.5, PDF p36 | 1912 × 780 | Full image | Supports the collection stage before dashboard presentation |
| [Zabbix test state](../assets/monitoring/zabbix-incident-state.png) | Figure 5.7, PDF p51 | 1912 × 973 | Full image | Preserves the actual anomaly and surrounding collection state |
| [DMZ rule order](../assets/firewall/dmz-rule-order.png) | Figure 4.10, PDF p38; same policy pictured on presentation slide 14 | 1035 × 345 | `(50, 65, 1085, 410)` from 1117 × 500 | Shows the LAN block above the outbound allow rule |
| [Windows agent editor](../assets/firewall/windows-agent-rule-editor.png) | Figure 4.12, PDF p40 | 1028 × 694 | `(12, 18, 1040, 712)` from 1110 × 828 | Retains the rule fields and visible port discrepancy |
| [SNMP editor](../assets/firewall/snmp-rule-editor.png) | Figure 4.13, PDF p40 | 1025 × 694 | `(10, 18, 1035, 712)` from 1098 × 797 | Shows the collector, pfSense destination, and UDP 161 |
| [DMZ connectivity](../assets/security-tests/dmz-connectivity.png) | Figure 4.11, PDF p39 | 872 × 351 | Full image | Shows the paired LAN and external ping outcomes |
| [Suricata alerts](../assets/security-tests/suricata-alerts.png) | Figure 5.4, PDF p49 | 877 × 645 | `(48, 72, 925, 717)` from 935 × 737 | Preserves repeated stream alerts with the log-view context |
| [hping3 result](../assets/security-tests/hping3-result.png) | Figure 5.5, PDF p49 | 758 × 218 | `(22, 78, 780, 296)` from 785 × 336 | Keeps the command, flood-mode caveat, and counters together |
| [Earlier blocked hosts](../assets/security-tests/blocked-hosts.png) | Figure 5.6, PDF p50 | 857 × 347 | `(175, 426, 1032, 773)` from 1556 × 946 | Retains both listed hosts, including the monitoring server |
| [Suricata interfaces](../assets/security-tests/suricata-interfaces.png) | Slide 18 video, **00:54.983333** | 2292 × 686 | `(840, 594, 3132, 1280)` | Shows running WAN and DMZ instances and their legacy mode |
| [Demo blocked host](../assets/security-tests/demo-blocked-host.png) | Slide 18 video, **01:34.983333** | 2281 × 417 | `(844, 1375, 3125, 1792)` | Shows the WAN-side test address and scan-related entry |
| [Completed WAN scan](../assets/security-tests/nmap-wan-result.png) | Slide 18 video, **01:44.983333** | 2915 × 650 | `(85, 110, 3000, 760)` | Adds completed scan evidence absent from the report's Nmap capture |

The Kali address is also corroborated by presentation slide 11 and the interface output below the selected scan result in the uncropped demo frame. The published scan crop focuses on the completed result; it does not include that lower interface output.

## How the visuals are used

The README opens with the actual monitoring interface, then places policy, connectivity, scan, and block-list evidence beside the related explanation. Secondary screenshots appear in the supporting documents or a collapsible section. Images can be opened at native resolution for small text.

The English Mermaid diagram is an explanatory redraw based on the address plan and detailed monitoring descriptions. It does not reproduce the original diagram's ambiguous monitoring arrows as literal packet directions.

## Material kept outside the repository

The full report, presentation, embedded video, extracted source images, and working previews are not committed. They contain unnecessary page layout, desktop context, and repeated setup material. The repository also excludes generic tool logos, school branding, planning charts, and installation-only screenshots that do not materially strengthen the engineering story.

The selected crops contain private lab addresses and virtual-machine identifiers as technical context. They were inspected for passwords, private keys, tokens, personal inbox details, and account credentials. No such material is included in the published set. The credential prompt visible in the hping3 terminal does not expose a password.

No deployment exports were supplied. The repository's policy tables and diagrams are documentation, not generated substitutes for original configuration files.
