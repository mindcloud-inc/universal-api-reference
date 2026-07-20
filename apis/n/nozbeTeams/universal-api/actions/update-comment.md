# Nozbe Teams: Update Comment

Updates an existing comment in Nozbe Teams.

```
PUT https://connect.mindcloud.co/v1/universal/nozbeTeams/latest/actions/update-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nozbe Teams `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/nozbeTeams/latest/actions/update-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/nozbeTeams/latest/actions/update-comment', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The comment to update. |
| `body` | string | no | The updated comment text. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authorId": "string",
      "body": "string",
      "createdAt": 1,
      "extra": "string",
      "id": "string",
      "isDeleted": true,
      "isPinned": true,
      "isTeam": true,
      "taskId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authorId` | string |  |
| `body` | string |  |
| `createdAt` | number |  |
| `extra` | string |  |
| `id` | string |  |
| `isDeleted` | boolean |  |
| `isPinned` | boolean |  |
| `isTeam` | boolean |  |
| `taskId` | string |  |

## Native endpoint

Through the native Nozbe Teams API, this operation is `PUT /comments/:id` (base URL `https://api4.nozbe.com/v1/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-comment.md) for the provider-specific parameters and requirements.

