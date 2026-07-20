# Socialbu: Connect Account

Connects a new social account to SocialBu.

```
POST https://connect.mindcloud.co/v1/universal/socialbu/latest/actions/connect-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Socialbu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/socialbu/latest/actions/connect-account" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/socialbu/latest/actions/connect-account', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "name": "Ava Chen",
      "provider": "string",
      "status": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `name` | string |  |
| `provider` | string |  |
| `status` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Socialbu API, this operation is `POST /accounts` (base URL `https://socialbu.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/connect-account.md) for the provider-specific parameters and requirements.

