# <img src="https://images.mindcloud.co/apps/icons/p-imms_1774897000373.png" alt="PIMMS logo" width="28" height="28"> PIMMS: Universal API

Create deep links and track conversions, analytics, and referrals

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/pIMMS/latest
- **Category:** Marketing
- **Actions:** 7
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://pimms.io
- **Vendor API docs:** https://pimms.apidocumentation.com/reference

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Retrieve QR Code](actions/retrieve-qr-code.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pIMMS/latest/actions/retrieve-qr-code?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (7)

### Analytics

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve Analytics](actions/retrieve-analytics.md) | GET | Retrieves filtered analytics metrics from PIMMS. |

### Lead

| Action | Method | Description |
| --- | --- | --- |
| [Track Lead](actions/track-lead.md) | POST | Creates a new tracked lead event in PIMMS. |

### Link

| Action | Method | Description |
| --- | --- | --- |
| [Create Link](actions/create-link.md) | POST | Creates a new deep link in PIMMS. |
| [Upsert Link](actions/upsert-link.md) | PUT | Updates an existing deep link in PIMMS, or creates one. |

### Qr Code

| Action | Method | Description |
| --- | --- | --- |
| [Retrieve QR Code](actions/retrieve-qr-code.md) | GET | Retrieves a QR code image from PIMMS. |

### Referrals Embed Token

| Action | Method | Description |
| --- | --- | --- |
| [Create Referrals Embed Token](actions/create-referrals-embed-token.md) | POST | Creates a new referrals embed token in PIMMS. |

### Sale

| Action | Method | Description |
| --- | --- | --- |
| [Track Sale](actions/track-sale.md) | POST | Creates a new tracked sale event in PIMMS. |

