
# Wireshark Malicious Traffic Analysis

## Project Overview
This project demonstrates the analysis of malicious network traffic using Wireshark, inspired by Chris Greer's video tutorial. The analysis focuses on DNS filtering, HTTP traffic inspection, GeoIP configuration, and data extraction from a malicious PCAP file containing **real live malware**. These skills are essential for Security Analysts working in threat detection and response.

---

## Skills Demonstrated
1. **DNS Filtering**: Identifying malicious domains by analyzing DNS queries and responses.
2. **HTTP Traffic Analysis**: Inspecting requests and responses to find leaked data (e.g., usernames, passwords, and system information).
3. **GeoIP Mapping**: Mapping attacker IP addresses to geographic locations using Wireshark's GeoIP database.
4. **File Extraction**: Recovering hidden executables and sensitive data from network traffic.

---

## Steps Followed
1. **DNS Analysis**:
   - Filtered DNS queries using `dns.qry.name contains "malicious-domain.com"`.
   - Identified suspicious domains and resolved their IP addresses.

2. **HTTP Requests and Data Extraction**:
   - Applied HTTP filters (e.g., `http.request.method == "POST"`) to detect sensitive data leaks.
   - Exported usernames, passwords, and hidden files from HTTP responses.

3. **GeoIP Configuration**:
   - Configured Wireshark to use the GeoIP database.
   - Mapped source and destination IP addresses to geographic locations for attacker analysis.

4. **File Extraction**:
   - Extracted hidden executables using Wireshark’s file export feature.
   - Verified files using hash tools to detect known malware signatures.

---

## Tools Used
- **Wireshark**: For packet analysis, filtering, and exporting data.
- **Python**: For automating file extraction and GeoIP lookups.
- **GeoIP Database**: For mapping IP addresses to geographic locations.

---

## Repository Structure
```
Wireshark-Malicious-Traffic-Analysis
├── README.md
├── PCAPs/
│   ├── malicious_sample.pcap (link to source)
│   ├── normal_traffic.pcap (optional, for comparison)
├── analysis/
│   ├── dns_analysis.md
│   ├── http_analysis.md
│   ├── geoip_mapping.md
│   ├── exported_data/
│   │   ├── usernames_passwords.txt
│   │   ├── system_info.txt
│   │   ├── hidden_exe.md
│   ├── screenshots/
│   │   ├── dns_filter.png
│   │   ├── http_requests.png
│   │   ├── geoip_example.png
├── scripts/
│   ├── extract_hidden_exe.py
│   ├── automate_geoip.py
├── LICENSE
└── .gitignore
```

---

## Sample Analysis and Findings
### DNS Analysis
- Filtered traffic using `dns.qry.name contains "malicious-domain.com"`.
- Identified suspicious domains resolving to known malicious IPs (e.g., `203.0.113.45`).

### HTTP Traffic Analysis
- Inspected HTTP POST requests leaking sensitive data:
  - **Exported Data**:
    - Username: `admin`
    - Password: `password123`
  - Hidden file URL: `http://malicious-site.com/hidden.exe`

### GeoIP Mapping
- Configured GeoIP to analyze attacker locations:
  - **Example Result**:
    - Attacker IP: `203.0.113.45` → Location: New York, USA

---

## How to Use This Repository
1. **Clone the Repository**:
   ```bash
   git clone https://github.com/yourusername/Wireshark-Malicious-Traffic-Analysis.git
   ```

2. **PCAP Analysis**:
   - Open `malicious_sample.pcap` in Wireshark.
   - Follow the steps in `analysis/dns_analysis.md` and `http_analysis.md`.

3. **Run Scripts**:
   - Use `scripts/extract_hidden_exe.py` to automate file extraction from the PCAP.
   - Run `scripts/automate_geoip.py` to map IP addresses.

---

## Resources
- [Chris Greer’s Video Tutorial](https://www.youtube.com/watch?v=M8yoYmiL7rA)
- [Malware Traffic Analysis PCAPs](https://malware-traffic-analysis.net/) (Password: `infected`)
- [Wireshark Documentation](https://www.wireshark.org/docs/)

---

## License
This project is licensed under the MIT License. See `LICENSE` for details.
