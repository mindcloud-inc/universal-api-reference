# Mural: Update Room

Updates an existing room in Mural.

```
PUT https://connect.mindcloud.co/v1/universal/mural/latest/actions/update-room
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mural `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mural/latest/actions/update-room" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "roomId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mural/latest/actions/update-room', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "roomId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `roomId` | number | yes |  |
| `name` | string | no |  |
| `roomType` | string | no |  |
| `description` | string | no |  |
| `favorite` | boolean | no |  |

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

Through the native Mural API, this operation is `PATCH /rooms/:roomId` (base URL `https://app.mural.co/api/public/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-room.md) for the provider-specific parameters and requirements.

