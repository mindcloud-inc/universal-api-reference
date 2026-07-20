# Socket: Rotate API Token

Rotates an existing API token in Socket.

```
PUT https://connect.mindcloud.co/v1/universal/socket/latest/actions/rotate-api-token
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Socket `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/socket/latest/actions/rotate-api-token" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/socket/latest/actions/rotate-api-token', {
  method: 'PUT',
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
      "createdBy": "string",
      "groupUuid": "string",
      "hash": "string",
      "id": "string",
      "token": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdBy` | string | ID of the Socket user who created the API Token |
| `groupUuid` | string | The stable group UUID (unchanged after rotation) |
| `hash` | string |  |
| `id` | string | The database ID of the new API token |
| `token` | string |  |

## Native endpoint

Through the native Socket API, this operation is `POST /orgs/:org_slug/api-tokens/rotate` (base URL `https://api.socket.dev/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/rotate-api-token.md) for the provider-specific parameters and requirements.

