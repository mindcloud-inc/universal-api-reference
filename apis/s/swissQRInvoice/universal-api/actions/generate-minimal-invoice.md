# Swiss QR Invoice: Generate Minimal Invoice

Creates a minimal Swiss QR invoice in Magic Heidi.

```
POST https://connect.mindcloud.co/v1/universal/swissQRInvoice/latest/actions/generate-minimal-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Swiss QR Invoice `connectionId` ([setup](../authentication.md)).

## Example request

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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data` | object | yes | Invoice data object nested under the documented top-level `data` request field. Edit the example values as needed. Default: `{"user_details":{"zip":"8001","city":"Zurich","iban":"CH0700700112900411647","name":"MindCloud GmbH","address":"Bahnhofstrasse 1"},"invoice_items":[{"quantity":1,"unit_price":149.5,"description":"Platform subscription"}],"customer_details":{"zip":"1204","city":"Geneva","name":"Sample Customer AG","address":"Rue du Rhone 1"}}`. |

## Response

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

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `expires` | number | Unix epoch milliseconds when the PDF URL expires. |
| `uid` | string | Invoice generation identifier. |
| `url` | string | Signed PDF download URL. |

## Native endpoint

Through the native Swiss QR Invoice API, this operation is `POST /create_invoice_abstract_v1d` (base URL `https://europe-west6-magic-heidi.cloudfunctions.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-minimal-invoice.md) for the provider-specific parameters and requirements.

