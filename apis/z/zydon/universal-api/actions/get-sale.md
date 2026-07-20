# Zydon: Get Sale

Retrieves sale details from Zydon.

```
GET https://connect.mindcloud.co/v1/universal/zydon/latest/actions/get-sale
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zydon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zydon/latest/actions/get-sale?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zydon/latest/actions/get-sale?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "payments": [
        {}
      ],
      "total_value": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date | Timestamp when the sale was created. |
| `id` | string | Sale identifier. |
| `payments` | array<object> | Payments associated with the sale. |
| `total_value` | number | Total sale value. |

## Native endpoint

Through the native Zydon API, this operation is `GET /sales/{id}` (base URL `https://api.zydon.com.br/api/sales`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-sale.md) for the provider-specific parameters and requirements.

