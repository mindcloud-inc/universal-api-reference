# Billingo: Get Partner



```
GET https://connect.mindcloud.co/v1/universal/billingo/latest/actions/get-partner
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Billingo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/billingo/latest/actions/get-partner?connectionId=$CONNECTION_ID&id=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "0"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/billingo/latest/actions/get-partner?${params}`, {
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
| `id` | number | yes | Billingo partner ID from the path. Default: `0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": {},
      "emails": [
        "ava@example.com"
      ],
      "iban": "string",
      "id": 1,
      "name": "Ava Chen",
      "phone": "string",
      "swift": "string",
      "taxcode": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | object |  |
| `emails` | array<string> |  |
| `iban` | string |  |
| `id` | number |  |
| `name` | string |  |
| `phone` | string |  |
| `swift` | string |  |
| `taxcode` | string |  |

## Native endpoint

Through the native Billingo API, this operation is `GET /partners/:id` (base URL `https://api.billingo.hu/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-partner.md) for the provider-specific parameters and requirements.

