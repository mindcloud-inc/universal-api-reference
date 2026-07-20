# ContentStudio: List Post Comments

Retrieves comments for a post from ContentStudio.

```
GET https://connect.mindcloud.co/v1/universal/contentStudio/latest/actions/list-post-comments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ContentStudio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/contentStudio/latest/actions/list-post-comments?connectionId=$CONNECTION_ID&post_id=string&workspace_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "post_id": "string",
  "workspace_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/contentStudio/latest/actions/list-post-comments?${params}`, {
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
| `page` | number | no | Page number for pagination. |
| `per_page` | number | no | Number of items per page. |
| `post_id` | string | yes | ContentStudio post ID. |
| `workspace_id` | string | yes | ContentStudio workspace ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "author": {},
      "comment": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "Id": "string",
      "isNote": true,
      "mentionedUsers": [
        "string"
      ],
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `author` | object |  |
| `comment` | string |  |
| `createdAt` | date |  |
| `Id` | string |  |
| `isNote` | boolean |  |
| `mentionedUsers` | array<string> |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native ContentStudio API, this operation is `GET /workspaces/:workspace_id/posts/:post_id/comments` (base URL `https://api.contentstudio.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-post-comments.md) for the provider-specific parameters and requirements.

