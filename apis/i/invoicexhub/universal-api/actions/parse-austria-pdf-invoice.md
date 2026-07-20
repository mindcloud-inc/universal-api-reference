# Invoice.xhub: Parse Austria PDF Invoice



```
GET https://connect.mindcloud.co/v1/universal/invoicexhub/latest/actions/parse-austria-pdf-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Invoice.xhub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/invoicexhub/latest/actions/parse-austria-pdf-invoice?connectionId=$CONNECTION_ID&data=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "data": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/invoicexhub/latest/actions/parse-austria-pdf-invoice?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data` | string | yes | Encoded invoice payload to parse. |
| `filename` | string | no | Optional original filename for format detection hints. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errors": [
        {}
      ],
      "format": "string",
      "hash": "string",
      "invoice": {},
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
| `errors` | array<object> |  |
| `format` | string |  |
| `hash` | string |  |
| `invoice` | object |  |
| `success` | boolean |  |
| `warnings` | array<object> |  |

## Native endpoint

Through the native Invoice.xhub API, this operation is `POST /api/v1/invoice/AT/pdf/parse` (base URL `https://service.invoice-api.xhub.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/parse-austria-pdf-invoice.md) for the provider-specific parameters and requirements.

