# Bolna: Get User Details

Retrieves your Bolna account details and usage limits.

```
GET https://connect.mindcloud.co/v1/universal/bolna/latest/actions/get-user-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bolna `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bolna/latest/actions/get-user-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bolna/latest/actions/get-user-details?${params}`, {
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
      "bypassCompliance": true,
      "concurrency": {},
      "email": "ava@example.com",
      "id": "string",
      "name": "Ava Chen",
      "pricing": {},
      "tierPlan": "string",
      "wallet": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bypassCompliance` | boolean |  |
| `concurrency` | object |  |
| `email` | string |  |
| `id` | string |  |
| `name` | string |  |
| `pricing` | object |  |
| `tierPlan` | string |  |
| `wallet` | number |  |

## Native endpoint

Through the native Bolna API, this operation is `GET /user/me` (base URL `https://api.bolna.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-details.md) for the provider-specific parameters and requirements.

