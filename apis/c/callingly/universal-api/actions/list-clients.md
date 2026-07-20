# Callingly: List Clients

Retrieves clients from Callingly.

```
GET https://connect.mindcloud.co/v1/universal/callingly/latest/actions/list-clients
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Callingly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/callingly/latest/actions/list-clients?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/callingly/latest/actions/list-clients?${params}`, {
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
      "billed_numbers": 1,
      "billed_users": 1,
      "email": "ava@example.com",
      "id": 1,
      "is_active": true,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `billed_numbers` | number |  |
| `billed_users` | number |  |
| `email` | string |  |
| `id` | number |  |
| `is_active` | boolean |  |
| `name` | string |  |

## Native endpoint

Through the native Callingly API, this operation is `GET /v1/clients` (base URL `https://api.callingly.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-clients.md) for the provider-specific parameters and requirements.

