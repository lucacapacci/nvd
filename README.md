# NIST NVD Mirror
This repository contains a continuously updated mirror of the CVEs at [NIST National Vulnerability Database (NVD)](https://nvd.nist.gov/) in JSON format. The data is updated every 2 hours and organized by year and CVE ID.

## Repository Structure

CVE data is stored under:

```
cve/{year}/CVE-{year}-{id}.json
```

### Example

To access CVE-2025-0001:

```
https://lucacapacci.github.io/nvd/cve/2025/CVE-2025-0001.json
```

## Usage Examples

### Using `curl`

```bash
curl -L https://lucacapacci.github.io/nvd/cve/2025/CVE-2025-0001.json
```

### Using Python

```python
import requests

url = "https://lucacapacci.github.io/nvd/cve/2025/CVE-2025-0001.json"
response = requests.get(url)
cve_data = response.json()

print(cve_data["cve"])
```

## Update Frequency

Data is updated automatically every **2 hours**, providing near real-time access to CVE information.


## Acknowledgments

This repository is strongly inspired by https://github.com/espressif/esp-nvd-mirror
