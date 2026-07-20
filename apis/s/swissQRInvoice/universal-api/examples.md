# Swiss QR Invoice Universal API Examples

These examples use the MindCloud API key and Swiss QR Invoice connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Generate Minimal Invoice

Creates a minimal Swiss QR invoice in Magic Heidi.

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

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/swissQRInvoice/latest/actions/generate-minimal-invoice', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data": {"user_details":{"zip":"8001","city":"Zurich","iban":"CH0700700112900411647","name":"MindCloud GmbH","address":"Bahnhofstrasse 1"},"invoice_items":[{"quantity":1,"unit_price":149.5,"description":"Platform subscription"}],"customer_details":{"zip":"1204","city":"Geneva","name":"Sample Customer AG","address":"Rue du Rhone 1"}}
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "expires": 1,
      "uid": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Generate Minimal Invoice action reference](actions/generate-minimal-invoice.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/swissQRInvoice/latest/actions/generate-minimal-invoice).
