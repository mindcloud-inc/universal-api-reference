# Jostle: List Task Comments



```
GET https://connect.mindcloud.co/v1/universal/jostle/latest/actions/list-task-comments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Jostle `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jostle/latest/actions/list-task-comments?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jostle/latest/actions/list-task-comments?${params}`, {
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
| `id` | string | yes | Id of the task |
| `count` | string | no | Maximum number of results to return per page Default: `20`. |
| `offset` | string | no | Offset to receive additional pages of content Default: `0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "commentId": "string",
      "commentText": "string",
      "createdDate": "string",
      "hasAttachment": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `commentId` | string |  |
| `commentText` | string |  |
| `createdDate` | string |  |
| `hasAttachment` | boolean |  |

## Native endpoint

Through the native Jostle API, this operation is `GET /v2/tasks/task/:id/comments` (base URL `https://api-prod.jostle.us`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-task-comments.md) for the provider-specific parameters and requirements.

