# zipBoard: Update Feedback

Updates an existing feedback comment in zipBoard.

```
PUT https://connect.mindcloud.co/v1/universal/zipBoard/latest/actions/update-feedback
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a zipBoard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zipBoard/latest/actions/update-feedback" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zipBoard/latest/actions/update-feedback', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `description` | string | no | Updated feedback description. |
| `id` | string | yes | Feedback record ID to update. |
| `title` | string | yes | Updated feedback title. |

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

Through the native zipBoard API, this operation is `PUT /issues/comments/:id` (base URL `https://app.zipboard.co/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-feedback.md) for the provider-specific parameters and requirements.

