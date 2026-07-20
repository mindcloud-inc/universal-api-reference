# Invoice.xhub: Generate Netherlands UBL Invoice



```
POST https://connect.mindcloud.co/v1/universal/invoicexhub/latest/actions/generate-netherlands-ubl-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Invoice.xhub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/invoicexhub/latest/actions/generate-netherlands-ubl-invoice" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "invoice": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/invoicexhub/latest/actions/generate-netherlands-ubl-invoice', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "invoice": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `invoice` | object | yes | Invoice payload to generate the document from. |
| `formatOptions` | object | no | Optional format-specific generation options. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": "string",
      "errors": [
        {}
      ],
      "filename": "Ava Chen",
      "format": "string",
      "hash": "string",
      "mimeType": "string",
      "success": true,
      "warnings": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | string |  |
| `errors` | array<object> |  |
| `filename` | string |  |
| `format` | string |  |
| `hash` | string |  |
| `mimeType` | string |  |
| `success` | boolean |  |
| `warnings` | array<object> |  |

## Native endpoint

Through the native Invoice.xhub API, this operation is `POST /api/v1/invoice/NL/UBL/generate` (base URL `https://service.invoice-api.xhub.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-netherlands-ubl-invoice.md) for the provider-specific parameters and requirements.

