# Assembly.com: Create Note

Creates a note in Assembly.com.

```
POST https://connect.mindcloud.co/v1/universal/assemblycom/latest/actions/create-note
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Assembly.com `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/assemblycom/latest/actions/create-note" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "entityType": "string",
  "entityId": "string",
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/assemblycom/latest/actions/create-note', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "entityType": "string",
    "entityId": "string",
    "title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `entityType` | string | yes | The type of entity that this note is associated with. |
| `entityId` | string | yes | The ID of the entity that this note is associated with. |
| `title` | string | yes | The note title. |
| `content` | string | no | The note content as valid HTML. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "content": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "creatorId": "string",
      "entityId": "string",
      "entityType": "string",
      "id": "string",
      "object": "string",
      "title": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `content` | string |  |
| `createdAt` | date |  |
| `creatorId` | string |  |
| `entityId` | string |  |
| `entityType` | string |  |
| `id` | string |  |
| `object` | string |  |
| `title` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Assembly.com API, this operation is `POST /notes` (base URL `https://api.assembly.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-note.md) for the provider-specific parameters and requirements.

