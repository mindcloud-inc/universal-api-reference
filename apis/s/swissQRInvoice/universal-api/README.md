# <img src="https://images.mindcloud.co/apps/icons/images-22_1774872655881.png" alt="Swiss QR Invoice logo" width="28" height="28"> Swiss QR Invoice: Universal API

Generate Swiss QR invoices and QR payment slips through Magic Heidi's Swiss QR Invoice API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/swissQRInvoice/latest
- **Category:** Commerce / Accounting
- **Actions:** 1
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://magicheidi.ch/qr-invoice-developer-api
- **Vendor API docs:** https://magicheidi.ch/qr-invoice-developer-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Generate Minimal Invoice](actions/generate-minimal-invoice.md):

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/swissQRInvoice/latest/actions/generate-minimal-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data": {
    "user_details": {
      "zip": "8001",
      "city": "Zurich",
      "iban": "CH0700700112900411647",
      "name": "MindCloud GmbH",
      "address": "Bahnhofstrasse 1"
    },
    "invoice_items": [
      {
        "quantity": 1,
        "unit_price": 149.5,
        "description": "Platform subscription"
      }
    ],
    "customer_details": {
      "zip": "1204",
      "city": "Geneva",
      "name": "Sample Customer AG",
      "address": "Rue du Rhone 1"
    }
  }
}'
```

## Actions (1)

### Invoice

| Action | Method | Description |
| --- | --- | --- |
| [Generate Minimal Invoice](actions/generate-minimal-invoice.md) | POST | Creates a minimal Swiss QR invoice in Magic Heidi. |

