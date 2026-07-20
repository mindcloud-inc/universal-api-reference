# <img src="https://images.mindcloud.co/apps/icons/output-onlinepngtools_1776172809634.png" alt="CodeQR - Link and QR Analytics logo" width="28" height="28"> CodeQR - Link and QR Analytics: Universal API

Create, manage, and analyze QR codes, links, and domains

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/codeQRLinkAndQRAnalytics/latest
- **Category:** Marketing
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://codeqr.io
- **Vendor API docs:** https://docs.codeqr.io/api-reference/introduction

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Projects](actions/list-projects.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/codeQRLinkAndQRAnalytics/latest/actions/list-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Analytics

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Analytics](actions/retrieve-analytics.md) | GET | Retrieves analytics from CodeQR. |

### Domain

| Action | Method | Description |
| --- | --- | --- |
| [Create Domain](actions/create-domain.md) | POST | Creates a domain in CodeQR. |
| [Delete Domain](actions/delete-domain.md) | DELETE | Deletes a domain from CodeQR. |
| [List Domains](actions/list-domains.md) | GET | Retrieves domains from CodeQR. |
| [Update Domain](actions/update-domain.md) | PUT | Updates a domain in CodeQR. |

### Event

| Action | Method | Description |
| --- | --- | --- |
| [List Events](actions/list-events.md) | GET | Retrieves events from CodeQR. |

### Link

| Action | Method | Description |
| --- | --- | --- |
| [Create Link](actions/create-link.md) | POST | Creates a link in CodeQR. |
| [Delete Link](actions/delete-link.md) | DELETE | Deletes a link from CodeQR. |
| [Get Link](actions/get-link.md) | GET | Retrieves a link from CodeQR. |
| [List Links](actions/list-links.md) | GET | Retrieves links from CodeQR. |
| [Update Link](actions/update-link.md) | PUT | Updates a link in CodeQR. |
| [Upsert Link](actions/upsert-link.md) | PUT | Updates or creates a link in CodeQR. |

### Project

| Action | Method | Description |
| --- | --- | --- |
| [Get Project](actions/get-project.md) | GET | Retrieves a project from CodeQR. |
| [List Projects](actions/list-projects.md) | GET | Retrieves projects from CodeQR. |

### Qrcode

| Action | Method | Description |
| --- | --- | --- |
| [Create QR Code](actions/create-qr-code.md) | POST | Creates a QR code in CodeQR. |
| [Delete QR Code](actions/delete-qr-code.md) | DELETE | Deletes a QR code from CodeQR. |
| [Get QR Code](actions/get-qr-code.md) | GET | Retrieves a QR code from CodeQR. |
| [List QR Codes](actions/list-qr-codes.md) | GET | Retrieves QR codes from CodeQR. |
| [Update QR Code](actions/update-qr-code.md) | PUT | Updates a QR code in CodeQR. |
| [Upsert QR Code](actions/upsert-qr-code.md) | PUT | Updates or creates a QR code in CodeQR. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [Create Tag](actions/create-tag.md) | POST | Creates a tag in CodeQR. |
| [Delete Tag](actions/delete-tag.md) | DELETE | Deletes a tag from CodeQR. |
| [List Tags](actions/list-tags.md) | GET | Retrieves tags from CodeQR. |
| [Update Tag](actions/update-tag.md) | PUT | Updates a tag in CodeQR. |

