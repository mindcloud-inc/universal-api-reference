# Privy: Update Key Quorum

Updates an existing key quorum in Privy.

```
PUT https://connect.mindcloud.co/v1/universal/privy/latest/actions/update-key-quorum
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Privy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/privy/latest/actions/update-key-quorum" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "keyQuorumId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/privy/latest/actions/update-key-quorum', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "keyQuorumId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `keyQuorumId` | string | yes | Privy key quorum ID. |

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

Through the native Privy API, this operation is `PATCH /v1/key_quorums/{{keyQuorumId}}` (base URL `https://api.privy.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-key-quorum.md) for the provider-specific parameters and requirements.

