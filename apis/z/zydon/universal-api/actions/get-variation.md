# Zydon: Get Variation

Retrieves variation details from Zydon.

```
GET https://connect.mindcloud.co/v1/universal/zydon/latest/actions/get-variation
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zydon `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zydon/latest/actions/get-variation?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zydon/latest/actions/get-variation?${params}`, {
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
      "active": true,
      "id": "string",
      "name": "Ava Chen",
      "values": [
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
| `active` | boolean | Whether the variation is active. |
| `id` | string | Variation identifier. |
| `name` | string | Variation name. |
| `values` | array<object> | Variation values. |

## Native endpoint

Through the native Zydon API, this operation is `GET /variations/{id}` (base URL `https://api.zydon.com.br/api/sales`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-variation.md) for the provider-specific parameters and requirements.

