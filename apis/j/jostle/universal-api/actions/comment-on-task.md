# Jostle: Comment on Task



```
POST https://connect.mindcloud.co/v1/universal/jostle/latest/actions/comment-on-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jostle `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/jostle/latest/actions/comment-on-task" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "commentText": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/jostle/latest/actions/comment-on-task', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "commentText": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Id for the targeted task |
| `commentText` | string | yes | Comment text up to 2500 characters |

## Response

```json
{
  "success": true,
  "data": [
    {
      "commentId": "string",
      "createdDate": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `commentId` | string |  |
| `createdDate` | string |  |

## Native endpoint

Through the native Jostle API, this operation is `POST /v2/tasks/task/:id/comment` (base URL `https://api-prod.jostle.us`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/comment-on-task.md) for the provider-specific parameters and requirements.

