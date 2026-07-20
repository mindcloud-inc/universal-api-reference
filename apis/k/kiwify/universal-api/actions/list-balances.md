# Kiwify: List Balances

Retrieves balances from Kiwify.

```
GET https://connect.mindcloud.co/v1/universal/kiwify/latest/actions/list-balances
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kiwify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kiwify/latest/actions/list-balances?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kiwify/latest/actions/list-balances?${params}`, {
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
      "available": 1,
      "legal_entity_id": "string",
      "pending": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `available` | number |  |
| `legal_entity_id` | string |  |
| `pending` | number |  |

## Native endpoint

Through the native Kiwify API, this operation is `GET /v1/balance` (base URL `https://public-api.kiwify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-balances.md) for the provider-specific parameters and requirements.

