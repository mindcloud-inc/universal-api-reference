# <img src="https://images.mindcloud.co/apps/icons/cloudmersive-icon_1777489847981.png" alt="Cloudmersive Security logo" width="28" height="28"> Cloudmersive Security: Universal API

Detects and blocks security threats in strings, URLs, and IP addresses using Cloudmersive Security Threat Detection APIs.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/cloudmersiveSecurity/latest
- **Actions:** 9
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://cloudmersive.com/security-threat-detection-api
- **Vendor API docs:** https://api.cloudmersive.com/docs/security.asp

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Check IP Bot Status](actions/check-ip-bot-status.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudmersiveSecurity/latest/actions/check-ip-bot-status?connectionId=$CONNECTION_ID&ipAddress=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (9)

### Ip Bot Check Result

| Action | Method | Description |
| --- | --- | --- |
| [Check IP Bot Status](actions/check-ip-bot-status.md) | GET | Checks an IP address for bot threats in Cloudmersive Security. |

### Ip Threat Result

| Action | Method | Description |
| --- | --- | --- |
| [Check IP Threat](actions/check-ip-threat.md) | GET | Checks an IP address for threats in Cloudmersive Security. |

### Json Threat Detection Result

| Action | Method | Description |
| --- | --- | --- |
| [Detect JSON Insecure Deserialization](actions/detect-json-insecure-deserialization.md) | GET | Detects JSON insecure deserialization attacks in Cloudmersive Security. |

### Sql Injection Detection Result

| Action | Method | Description |
| --- | --- | --- |
| [Detect SQL Injection](actions/detect-sql-injection.md) | GET | Detects SQL injection threats in Cloudmersive Security. |

### Ssrf Url Threat Result

| Action | Method | Description |
| --- | --- | --- |
| [Detect SSRF URL Threat](actions/detect-ssrf-url-threat.md) | GET | Checks a URL for SSRF threats in Cloudmersive Security. |

### Threat Detection Result

| Action | Method | Description |
| --- | --- | --- |
| [Detect Threats in Text](actions/detect-threats-in-text.md) | GET | Detects threats in text with Cloudmersive Security. |

### Tor Node Check Result

| Action | Method | Description |
| --- | --- | --- |
| [Check Tor Exit Node](actions/check-tor-exit-node.md) | GET | Checks whether an IP is a Tor node in Cloudmersive Security. |

### Xss Detection Result

| Action | Method | Description |
| --- | --- | --- |
| [Detect and Normalize XSS](actions/detect-and-normalize-xss.md) | GET | Detects and normalizes XSS threats in Cloudmersive Security. |

### Xxe Detection Result

| Action | Method | Description |
| --- | --- | --- |
| [Detect XXE in XML](actions/detect-xxe-in-xml.md) | GET | Detects XXE threats in XML with Cloudmersive Security. |

