# Jostle: Attach File to Task Comment



```
POST https://connect.mindcloud.co/v1/universal/jostle/latest/actions/attach-file-to-task-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jostle `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/jostle/latest/actions/attach-file-to-task-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "taskId": "string",
  "commentId": "string",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/jostle/latest/actions/attach-file-to-task-comment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "taskId": "string",
    "commentId": "string",
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `taskId` | string | yes | Id of the targeted task |
| `commentId` | string | yes | Id of the targeted task comment |
| `url` | string | yes | URL pointing to a file to upload |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "requestId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object |  |
| `requestId` | string |  |

## Native endpoint

Through the native Jostle API, this operation is `POST /v2/tasks/task/:taskId/comment/:commentId/attachment` (base URL `https://api-prod.jostle.us`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/attach-file-to-task-comment.md) for the provider-specific parameters and requirements.

