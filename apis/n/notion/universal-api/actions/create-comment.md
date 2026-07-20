# Notion: Create Comment

Creates a new comment in Notion.

```
POST https://connect.mindcloud.co/v1/universal/notion/latest/actions/create-comment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Notion `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/notion/latest/actions/create-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "richText": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/notion/latest/actions/create-comment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "richText": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `parent` | object | no | Parent page or block object for a new comment thread. |
| `richText` | list<object> | yes | Comment content in Notion rich_text format. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `discussionId` | string | no | Existing discussion ID for a reply comment. |
| `attachments` | list<object> | no | Optional attachments for the comment. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdTime": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "lastEditedTime": "2026-05-07T12:00:00.000Z",
      "object": "string",
      "richText": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdTime` | date | Creation timestamp. |
| `id` | string | Comment identifier. |
| `lastEditedTime` | date | Last edit timestamp. |
| `object` | string | Returned object type. |
| `richText` | array<object> | Comment rich text payload. |

## Native endpoint

Through the native Notion API, this operation is `POST /comments` (base URL `https://api.notion.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-comment.md) for the provider-specific parameters and requirements.

