# Invoice.xhub: Validate Netherlands Invoice



```
GET https://connect.mindcloud.co/v1/universal/invoicexhub/latest/actions/validate-netherlands-invoice
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Invoice.xhub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/invoicexhub/latest/actions/validate-netherlands-invoice?connectionId=$CONNECTION_ID&xml=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "xml": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/invoicexhub/latest/actions/validate-netherlands-invoice?${params}`, {
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
| `xml` | string | yes | Invoice XML document to validate. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errors": [
        {}
      ],
      "valid": true,
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
| `valid` | boolean |  |
| `warnings` | array<object> |  |

## Native endpoint

Through the native Invoice.xhub API, this operation is `POST /api/v1/invoice/NL/validate` (base URL `https://service.invoice-api.xhub.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-netherlands-invoice.md) for the provider-specific parameters and requirements.

