# OPN: Get Chain Account

Retrieves account details for a chain from OPN.

```
GET https://connect.mindcloud.co/v1/universal/oPN/latest/actions/get-chain-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a OPN `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oPN/latest/actions/get-chain-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oPN/latest/actions/get-chain-account?${params}`, {
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
      "created_at": "string",
      "email": "ava@example.com",
      "id": "string",
      "key": "string",
      "livemode": true,
      "location": "string",
      "object": "string",
      "revoked": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string |  |
| `email` | string |  |
| `id` | string |  |
| `key` | string |  |
| `livemode` | boolean |  |
| `location` | string |  |
| `object` | string |  |
| `revoked` | boolean |  |

## Native endpoint

Through the native OPN API, this operation is `GET /chains/:id/account` (base URL `https://api.omise.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-chain-account.md) for the provider-specific parameters and requirements.

