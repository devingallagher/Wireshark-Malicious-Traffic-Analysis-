
## Investigation Workflow

### Extract Hashes from Malicious Files
- **Tools:** Wireshark, [Hash My Files](https://www.nirsoft.net/utils/hash_my_files.html)
- **Reference:** `questions.png`, `first_hash.png`, `second_hash.png`, `third_hash.png`, `get_hashes.png`
- **Purpose:** Extracting hashes helps identify known malware by comparing them against virus databases like VirusTotal.

### Identify Malicious Domains and URLs
- **Tools:** Wireshark, VirusTotal
- **Reference:** `questions.png`, `find_url_of_infected_sites.png`
- **Purpose:** Helps pinpoint infected domains serving malware, leading to further investigation of attack vectors.

### Analyze Protocol Hierarchy & HTTP Requests
- **Tools:** Wireshark Filters
- **Reference:** `questions.png`, `hierarchy_protocol_http_filter.png`, `http_request.png`
- **Purpose:** Understanding network communication patterns, detecting suspicious HTTP requests, and analyzing potential exploit delivery mechanisms.

### Extract MAC Addresses and Hostnames of Affected Devices
- **Tools:** Wireshark
- **Reference:** `questions.png`, `find_host_name.png`, `find_mac_address.png`
- **Purpose:** Identifying compromised devices on the network to facilitate remediation efforts.

### Analyze Exported Objects from Wireshark
- **Tools:** Wireshark Export Feature
- **Reference:** `questions.png`, `export.png`
- **Purpose:** Extracted files can be further analyzed for hidden malware, scripts, or exploits.

## Key Findings

- **Malicious Files Identified:**
  - **SWF Exploit:** `7b3baa7d6bb3720f369219789e38d6ab` (infected)
  - **Java Exploit:** `1e34fdebbf655ceba78b45e43520ddff` (infected)
  - **Clean File:** `d27c68dcdbdcdb674ee02496bc90d98` (not infected)

- **Infected Domain Identified:**
  - `stand.trustandprobate realty.com`

- **Source and Destination IPs:**
  - **Malicious Site IP:** `37.200.69.143`
  - **Infected Device IP:** `172.16.165.165`

- **Infected Machine Details:**
  - **Hostname:** `K34EN6W3N-PC`
  - **MAC Address:** `f0:19:af:02:9b:f1`

## Additional Resources

- [Wireshark Official Documentation](https://www.wireshark.org/docs/wsug_html_chunked/)
- [Malware Traffic Analysis](https://malware-traffic-analysis.net)
- [Hash My Files](https://www.nirsoft.net/utils/hash_my_files.html)

## How to Use This Repository

1. **Download and Open the Provided PCAP Files in Wireshark.**
2. **Use the Filters and Analysis Steps Described to Investigate Malicious Traffic.**
3. **Cross-check Findings with VirusTotal or Other Threat Intelligence Sources.**
4. **Export Objects and Hash Suspicious Files for Malware Identification.**

## Contributing

Contributions are welcome! Feel free to submit pull requests with improvements or additional analysis insights.

## Author

[devingallagher](https://github.com/devingallagher)
