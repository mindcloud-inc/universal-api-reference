# zipBoard: Create Feedback

Creates a new feedback comment in zipBoard.

```
POST https://connect.mindcloud.co/v1/universal/zipBoard/latest/actions/create-feedback
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a zipBoard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zipBoard/latest/actions/create-feedback" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string",
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zipBoard/latest/actions/create-feedback', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "string",
    "projectId": "string",
    "title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `description` | string | no | Optional feedback description. |
| `projectId` | string | yes | Project ID where the feedback should be created. |
| `projectId` | string | yes |  |
| `title` | string | yes | Feedback title. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "commentId": "string",
      "commentType": "string",
      "description": "string",
      "project_id": "string",
      "reply": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `commentId` | string | Comment identifier. |
| `commentType` | string | Comment type. |
| `description` | string | Feedback description. |
| `project_id` | string | Project identifier. |
| `reply` | string | Feedback reply. |
| `title` | string | Feedback title. |

## Native endpoint

Through the native zipBoard API, this operation is `POST /issues/comments` (base URL `https://app.zipboard.co/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-feedback.md) for the provider-specific parameters and requirements.

