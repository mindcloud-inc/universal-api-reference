# Nozbe Personal: List Comment Attachments

Retrieves attachments for a Nozbe Personal comment.

```
GET https://connect.mindcloud.co/v1/universal/nozbePersonal/latest/actions/list-comment-attachments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Nozbe Personal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nozbePersonal/latest/actions/list-comment-attachments?connectionId=$CONNECTION_ID&commentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "commentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nozbePersonal/latest/actions/list-comment-attachments?${params}`, {
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
| `commentId` | string | yes | Comment ID from Nozbe. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authorId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "extra": "string",
      "id": "string",
      "mimeType": "string",
      "name": "Ava Chen",
      "size": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authorId` | string |  |
| `createdAt` | date |  |
| `extra` | string |  |
| `id` | string |  |
| `mimeType` | string |  |
| `name` | string |  |
| `size` | number |  |
| `status` | string |  |

## Native endpoint

Through the native Nozbe Personal API, this operation is `GET /comments/:comment_id/attachments` (base URL `https://api4.nozbe.com/v1/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-comment-attachments.md) for the provider-specific parameters and requirements.

