# Project Bubble: Create Comment

Creates a new comment in a Project Bubble project.

```
POST https://connect.mindcloud.co/v1/universal/projectBubble/latest/actions/create-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Project Bubble `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/projectBubble/latest/actions/create-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "project_id": "string",
  "comment": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/projectBubble/latest/actions/create-comment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "project_id": "string",
    "comment": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `project_id` | string | yes |  |
| `comment` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Project Bubble API returns.

## Native endpoint

Through the native Project Bubble API, this operation is `POST /comments/:project_id` (base URL `https://api.projectbubble.com/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-comment.md) for the provider-specific parameters and requirements.

