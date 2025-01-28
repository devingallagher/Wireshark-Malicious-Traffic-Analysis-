# Wireshark Analysis and IOC Investigation

This repository provides a structured walkthrough of a Wireshark analysis tutorial, focusing on identifying Indicators of Compromise (IOCs) and investigating malicious network activity. It documents key steps for network forensics and traffic analysis.

## Repository Structure

```
Wireshark-IOC-Investigation
├── README.md                   # Main documentation
├── PCAPs/                      # PCAP files if available
├── analysis/                    # In-depth analysis
│   ├── infected_files.png       # Extracted hashes from infected files
│   ├── infected_sites.png       # Domains and URLs of malicious websites
│   ├── protocol_analysis.png    # Protocol hierarchy and filter usage
│   ├── http_requests.png        # HTTP request analysis with packet details
│   ├── mac_addresses.png        # Extracted MAC addresses of infected machines
│   ├── hostnames.png            # Extracted hostnames from network traffic
│   ├── wireshark_exports.png    # Exported objects from Wireshark
├── images/                      # Screenshots and supporting images
│   ├── questions.png            # Investigation summary in one image
│   ├── first_hash.png           # VirusTotal scan of first hash
│   ├── second_hash.png          # VirusTotal scan of second hash
│   ├── third_hash.png           # VirusTotal scan of third hash
├── LICENSE                      # License details
└── .gitignore                   # Ignore unnecessary files
```

## Investigation Workflow

1. **Extract Hashes from Malicious Files**  
   - Tools: Wireshark, [Hash My Files](https://www.nirsoft.net/utils/hash_my_files.html)  
   - Reference: `questions.png`, `first_hash.png`, `second_hash.png`, `third_hash.png`

2. **Identify Malicious Domains and URLs**  
   - Tools: Wireshark, VirusTotal  
   - Reference: `questions.png`

3. **Analyze Protocol Hierarchy & HTTP Requests**  
   - Tools: Wireshark Filters  
   - Reference: `questions.png`

4. **Extract MAC Addresses and Hostnames of Affected Devices**  
   - Tools: Wireshark  
   - Reference: `questions.png`

5. **Analyze Exported Objects from Wireshark**  
   - Tools: Wireshark Export Feature  
   - Reference: `questions.png`

## Key Features

- **Investigation Summary:** All key findings documented in `questions.png`.
- **Extracted Hashes:** VirusTotal scan results stored in `first_hash.png`, `second_hash.png`, `third_hash.png`.
- **Identified Malicious Sites:** Infected domains and URLs included.
- **Protocol Analysis:** Understanding protocol hierarchy and applied filters.
- **HTTP Requests:** Packet details for suspicious HTTP requests.
- **MAC Addresses & Hostnames:** Extracted device identifiers for forensic analysis.
- **Wireshark Exports:** Object exports from network captures for deeper analysis.

## Additional Resources

- [Wireshark Official Documentation](https://www.wireshark.org/docs/wsug_html_chunked/)
- [Malware Traffic Analysis](https://malware-traffic-analysis.net)
- [Hash My Files](https://www.nirsoft.net/utils/hash_my_files.html)

## Contributing
