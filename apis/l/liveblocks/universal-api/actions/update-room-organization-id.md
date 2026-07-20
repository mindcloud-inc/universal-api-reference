# Liveblocks: Update Room Organization ID

Updates a room organization ID in Liveblocks.

```
PUT https://connect.mindcloud.co/v1/universal/liveblocks/latest/actions/update-room-organization-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Liveblocks `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/liveblocks/latest/actions/update-room-organization-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/liveblocks/latest/actions/update-room-organization-id', {
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `roomId` | string | no | ID of the room. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "defaultAccesses": [
        "string"
      ],
      "groupsAccesses": {},
      "id": "string",
      "lastConnectionAt": "string",
      "metadata": {},
      "type": "string",
      "usersAccesses": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string |  |
| `defaultAccesses` | array<string> |  |
| `groupsAccesses` | object |  |
| `id` | string |  |
| `lastConnectionAt` | string |  |
| `metadata` | object |  |
| `type` | string |  |
| `usersAccesses` | object |  |

## Native endpoint

Through the native Liveblocks API, this operation is `POST /rooms/:roomId/update-organization-id` (base URL `https://api.liveblocks.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-room-organization-id.md) for the provider-specific parameters and requirements.

