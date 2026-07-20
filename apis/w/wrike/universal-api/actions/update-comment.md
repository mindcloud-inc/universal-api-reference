# Wrike: Update Comment

Updates an existing comment in Wrike.

```
PUT https://connect.mindcloud.co/v1/universal/wrike/latest/actions/update-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Wrike `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/wrike/latest/actions/update-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "commentId": "string",
  "text": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wrike/latest/actions/update-comment', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "commentId": "string",
    "text": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `commentId` | string | yes | Wrike comment ID. |
| `text` | string | yes | Comment text, cannot be empty |
| `plainText` | boolean | no | Treat comment text as plain text |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authorId": "string",
      "createdDate": "2026-05-07T12:00:00.000Z",
      "direction": "string",
      "emailSubject": "ava@example.com",
      "folderId": "string",
      "id": "string",
      "taskId": "string",
      "text": "string",
      "type": "string",
      "updatedDate": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authorId` | string |  |
| `createdDate` | date |  |
| `direction` | string |  |
| `emailSubject` | string |  |
| `folderId` | string |  |
| `id` | string |  |
| `taskId` | string |  |
| `text` | string |  |
| `type` | string |  |
| `updatedDate` | date |  |

## Native endpoint

Through the native Wrike API, this operation is `PUT /comments/:commentId` (base URL `https://{{credentials.accessTokenRequest.host}}/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-comment.md) for the provider-specific parameters and requirements.

