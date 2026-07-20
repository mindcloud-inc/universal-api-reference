# Webex: Create Room

Creates a new room in Webex.

```
POST https://connect.mindcloud.co/v1/universal/webex/latest/actions/create-room
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webex `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/webex/latest/actions/create-room" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "title": "MindCloud Test Room"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/webex/latest/actions/create-room', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "title": "MindCloud Test Room"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | yes | Room title. Example: `MindCloud Test Room`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "2026-05-07T12:00:00.000Z",
      "creatorId": "string",
      "id": "string",
      "isLocked": true,
      "isPublic": true,
      "isReadOnly": true,
      "lastActivity": "2026-05-07T12:00:00.000Z",
      "ownerId": "string",
      "teamId": "string",
      "title": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date | Room creation timestamp. |
| `creatorId` | string | Person identifier for the room creator. |
| `id` | string | Room identifier. |
| `isLocked` | boolean | Whether the room is locked. |
| `isPublic` | boolean | Whether the room is public. |
| `isReadOnly` | boolean | Whether the room is read-only. |
| `lastActivity` | date | Timestamp of the most recent room activity. |
| `ownerId` | string | Organization identifier that owns the room. |
| `teamId` | string | Associated team identifier when the room belongs to a team. |
| `title` | string | Room title. |
| `type` | string | Room type. |

## Native endpoint

Through the native Webex API, this operation is `POST /rooms` (base URL `https://webexapis.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-room.md) for the provider-specific parameters and requirements.

