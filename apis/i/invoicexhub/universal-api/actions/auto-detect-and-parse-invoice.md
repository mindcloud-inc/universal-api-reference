# Invoice.xhub: Auto-Detect and Parse Invoice



```
GET https://connect.mindcloud.co/v1/universal/invoicexhub/latest/actions/auto-detect-and-parse-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Invoice.xhub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/invoicexhub/latest/actions/auto-detect-and-parse-invoice?connectionId=$CONNECTION_ID&data=JVBERi0xLjQKJUZha2VQREY%3D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "data": "JVBERi0xLjQKJUZha2VQREY="
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/invoicexhub/latest/actions/auto-detect-and-parse-invoice?${params}`, {
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
| `data` | string | yes | Base64-encoded invoice document content. Default: `JVBERi0xLjQKJUZha2VQREY=`. |
| `filename` | string | no | Optional filename used to hint format detection. Default: `sample.pdf`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "detection": {},
      "errors": [
        {}
      ],
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
| `detection` | object |  |
| `errors` | array<object> |  |
| `hash` | string |  |
| `invoice` | object |  |
| `success` | boolean |  |
| `warnings` | array<object> |  |

## Native endpoint

Through the native Invoice.xhub API, this operation is `POST /api/v1/invoice/parse` (base URL `https://service.invoice-api.xhub.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/auto-detect-and-parse-invoice.md) for the provider-specific parameters and requirements.

