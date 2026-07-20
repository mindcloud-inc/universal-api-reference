# Mural: Get Room

Retrieves a room from Mural by ID.

```
GET https://connect.mindcloud.co/v1/universal/mural/latest/actions/get-room
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mural `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mural/latest/actions/get-room?connectionId=$CONNECTION_ID&roomId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "roomId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mural/latest/actions/get-room?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `roomId` | number | yes | Unique identifier of a room. |

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

Through the native Mural API, this operation is `GET /rooms/:roomId` (base URL `https://app.mural.co/api/public/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-room.md) for the provider-specific parameters and requirements.

