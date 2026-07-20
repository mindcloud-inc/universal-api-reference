# Rye: Get Balance

Retrieves the drawdown balance from Rye.

```
GET https://connect.mindcloud.co/v1/universal/rye/latest/actions/get-balance
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rye `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rye/latest/actions/get-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rye/latest/actions/get-balance?${params}`, {
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
      "balance": {},
      "drawdownEnabled": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `balance` | object |  |
| `drawdownEnabled` | boolean |  |

## Native endpoint

Through the native Rye API, this operation is `GET /api/v1/billing/balance` (base URL `https://staging.api.rye.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-balance.md) for the provider-specific parameters and requirements.

