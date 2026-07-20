# Privy: Create Key Quorum

Creates a new key quorum in Privy.

```
POST https://connect.mindcloud.co/v1/universal/privy/latest/actions/create-key-quorum
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Privy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/privy/latest/actions/create-key-quorum" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/privy/latest/actions/create-key-quorum', {
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
      "authorization_keys": [
        {
          "display_name": "Ava Chen",
          "public_key": "string"
        }
      ],
      "authorization_threshold": 1,
      "display_name": "Ava Chen",
      "id": "string",
      "key_quorum_ids": [
        "string"
      ],
      "user_ids": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authorization_keys[].display_name` | string |  |
| `authorization_keys[].public_key` | string |  |
| `authorization_threshold` | number |  |
| `display_name` | string |  |
| `id` | string |  |
| `key_quorum_ids` | array<string> |  |
| `user_ids` | array<string> |  |

## Native endpoint

Through the native Privy API, this operation is `POST /v1/key_quorums` (base URL `https://api.privy.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-key-quorum.md) for the provider-specific parameters and requirements.

