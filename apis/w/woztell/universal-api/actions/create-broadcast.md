# Woztell: Create Broadcast

Creates a broadcast in your Woztell workspace.

```
POST https://connect.mindcloud.co/v1/universal/woztell/latest/actions/create-broadcast
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Woztell `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/woztell/latest/actions/create-broadcast" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/woztell/latest/actions/create-broadcast', {
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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `variables.input.name` | string | no |  |
| `variables.input.description` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "createBroadcast": {
          "broadcast": {
            "_id": "string",
            "appId": "string",
            "createdAt": 1,
            "description": "string",
            "etag": "string",
            "id": "string",
            "memberCount": 1,
            "name": "Ava Chen",
            "priority": 1,
            "readCount": 1,
            "scheduleAt": 1,
            "sentCount": 1,
            "updatedAt": 1
          },
          "clientMutationId": "string"
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.createBroadcast.broadcast._id` | string |  |
| `data.createBroadcast.broadcast.appId` | string |  |
| `data.createBroadcast.broadcast.createdAt` | number |  |
| `data.createBroadcast.broadcast.description` | string |  |
| `data.createBroadcast.broadcast.etag` | string |  |
| `data.createBroadcast.broadcast.id` | string |  |
| `data.createBroadcast.broadcast.memberCount` | number |  |
| `data.createBroadcast.broadcast.name` | string |  |
| `data.createBroadcast.broadcast.priority` | number |  |
| `data.createBroadcast.broadcast.readCount` | number |  |
| `data.createBroadcast.broadcast.scheduleAt` | number |  |
| `data.createBroadcast.broadcast.sentCount` | number |  |
| `data.createBroadcast.broadcast.updatedAt` | number |  |
| `data.createBroadcast.clientMutationId` | string |  |

## Native endpoint

Through the native Woztell API, this operation is `POST /` (base URL `https://open.api.woztell.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-broadcast.md) for the provider-specific parameters and requirements.

