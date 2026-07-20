# <img src="https://images.mindcloud.co/apps/icons/cloudmersive-icon_1777994645825.png" alt="Cloudmersive Virus Scan logo" width="28" height="28"> Cloudmersive Virus Scan: Universal API

Scan files, websites, and content with Cloudmersive Virus Scan to detect viruses, malware, and related security threats.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/cloudmersiveVirusScan/latest
- **Actions:** 3
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://cloudmersive.com/virus-api
- **Vendor API docs:** https://api.cloudmersive.com/docs/virus.asp

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Scan Website for Threats](actions/scan-website-for-threats.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudmersiveVirusScan/latest/actions/scan-website-for-threats?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (3)

### Advanced Virus Scan Result

| Action | Method | Description |
| --- | --- | --- |
| [Advanced Scan File for Viruses](actions/advanced-scan-file-for-viruses.md) | GET | Performs an advanced file virus scan with Cloudmersive Virus Scan. |

### Virus Scan Result

| Action | Method | Description |
| --- | --- | --- |
| [Scan File for Viruses](actions/scan-file-for-viruses.md) | GET | Scans a file for viruses with Cloudmersive Virus Scan. |

### Website Scan Result

| Action | Method | Description |
| --- | --- | --- |
| [Scan Website for Threats](actions/scan-website-for-threats.md) | GET | Scans a website for malicious content with Cloudmersive Virus Scan. |

