# <img src="https://images.mindcloud.co/apps/icons/favicon-www-opportify-ai-48x48_1776885315475.png" alt="Opportify logo" width="28" height="28"> Opportify: Universal API

Analyze emails and IPs for fraud and deliverability insights

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/opportify/latest
- **Category:** IT Operations / Security & Compliance
- **Actions:** 10
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://opportify.ai
- **Vendor API docs:** https://www.opportify.ai/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Analyze Email](actions/analyze-email.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/opportify/latest/actions/analyze-email?connectionId=$CONNECTION_ID&email=ava%40example.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (10)

### Email

| Action | Method | Description |
| --- | --- | --- |
| [Analyze Email](actions/analyze-email.md) | GET | Analyzes an email address in Opportify for deliverability and risk. |

### Email Batch Export Job

| Action | Method | Description |
| --- | --- | --- |
| [Create Email Batch Export](actions/create-email-batch-export.md) | POST | Creates an export job for email batch results in Opportify. |
| [Get Email Batch Export Status](actions/get-email-batch-export-status.md) | GET | Retrieves the status of an email batch export job in Opportify. |

### Email Batch Job

| Action | Method | Description |
| --- | --- | --- |
| [Batch Analyze Emails](actions/batch-analyze-emails.md) | POST | Creates an asynchronous email analysis job in Opportify. |
| [Get Email Batch Status](actions/get-email-batch-status.md) | GET | Retrieves the status of an email batch job in Opportify. |

### Ip Address

| Action | Method | Description |
| --- | --- | --- |
| [Analyze IP](actions/analyze-ip.md) | GET | Analyzes an IP address in Opportify for risk and geolocation. |

### Ip Batch Export Job

| Action | Method | Description |
| --- | --- | --- |
| [Create IP Batch Export](actions/create-ip-batch-export.md) | POST | Creates an export job for IP batch results in Opportify. |
| [Get IP Batch Export Status](actions/get-ip-batch-export-status.md) | GET | Retrieves the status of an IP batch export job in Opportify. |

### Ip Batch Job

| Action | Method | Description |
| --- | --- | --- |
| [Batch Analyze IPs](actions/batch-analyze-ips.md) | POST | Creates an asynchronous IP analysis job in Opportify. |
| [Get IP Batch Status](actions/get-ip-batch-status.md) | GET | Retrieves the status of an IP batch job in Opportify. |

