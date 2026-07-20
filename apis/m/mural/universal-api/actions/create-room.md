# Mural: Create Room

Creates a new room in Mural.

```
POST https://connect.mindcloud.co/v1/universal/mural/latest/actions/create-room
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mural `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mural/latest/actions/create-room" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceId": "string",
  "name": "Ava Chen",
  "roomType": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mural/latest/actions/create-room', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceId": "string",
    "name": "Ava Chen",
    "roomType": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspaceId` | string | yes |  |
| `name` | string | yes |  |
| `roomType` | string | yes |  |
| `description` | string | no |  |
| `confidential` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "confidential": true,
      "createdBy": {},
      "createdOn": 1,
      "description": "string",
      "favorite": true,
      "id": 1,
      "isMember": true,
      "name": "Ava Chen",
      "type": "string",
      "updatedBy": {},
      "updatedOn": 1,
      "workspaceId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `confidential` | boolean |  |
| `createdBy` | object |  |
| `createdOn` | number |  |
| `description` | string |  |
| `favorite` | boolean |  |
| `id` | number |  |
| `isMember` | boolean |  |
| `name` | string |  |
| `type` | string |  |
| `updatedBy` | object |  |
| `updatedOn` | number |  |
| `workspaceId` | string |  |

## Native endpoint

Through the native Mural API, this operation is `POST /rooms` (base URL `https://app.mural.co/api/public/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-room.md) for the provider-specific parameters and requirements.

