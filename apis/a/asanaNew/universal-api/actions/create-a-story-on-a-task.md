# Asana: Create a story on a task

Creates a story on a task in Asana.

```
POST https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/create-a-story-on-a-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Asana `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/create-a-story-on-a-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "taskGid": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/asanaNew/latest/actions/create-a-story-on-a-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "taskGid": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data.text` | string | no | The plain text of the comment to add. |
| `taskGid` | string | yes |  |
| `data` | object | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": {
        "gid": "string",
        "name": "Ava Chen",
        "resourceType": "string"
      },
      "gid": "string",
      "hearted": true,
      "isEditable": true,
      "isEdited": true,
      "isPinned": true,
      "liked": true,
      "numHearts": 1,
      "numLikes": 1,
      "resourceSubtype": "string",
      "resourceType": "string",
      "source": "string",
      "target": {
        "gid": "string",
        "name": "Ava Chen",
        "resourceSubtype": "string",
        "resourceType": "string"
      },
      "text": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date |  |
| `createdBy.gid` | string |  |
| `createdBy.name` | string |  |
| `createdBy.resourceType` | string |  |
| `gid` | string |  |
| `hearted` | boolean |  |
| `isEditable` | boolean |  |
| `isEdited` | boolean |  |
| `isPinned` | boolean |  |
| `liked` | boolean |  |
| `numHearts` | number |  |
| `numLikes` | number |  |
| `resourceSubtype` | string |  |
| `resourceType` | string |  |
| `source` | string |  |
| `target.gid` | string |  |
| `target.name` | string |  |
| `target.resourceSubtype` | string |  |
| `target.resourceType` | string |  |
| `text` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Asana API, this operation is `POST tasks/:task_gid/stories` (base URL `https://app.asana.com/api/1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-a-story-on-a-task.md) for the provider-specific parameters and requirements.

