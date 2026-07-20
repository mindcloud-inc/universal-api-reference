# ChangeCrab: Update Post

Updates an existing post in ChangeCrab.

```
PUT https://connect.mindcloud.co/v1/universal/changeCrab/latest/actions/update-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChangeCrab `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/changeCrab/latest/actions/update-post" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "e.g. product-updates",
  "postId": "e.g. 12345",
  "summary": "e.g. Released SSO support",
  "markdown": "Write the release notes in Markdown.",
  "public": "1",
  "team": "e.g. 101038"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/changeCrab/latest/actions/update-post', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "e.g. product-updates",
    "postId": "e.g. 12345",
    "summary": "e.g. Released SSO support",
    "markdown": "Write the release notes in Markdown.",
    "public": "1",
    "team": "e.g. 101038"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The ChangeCrab changelog access ID. Example: `e.g. product-updates`. |
| `postId` | number | yes | The ChangeCrab post ID. Example: `e.g. 12345`. |
| `summary` | string | yes | The post title or summary line. Example: `e.g. Released SSO support`. |
| `markdown` | string | yes | The Markdown body for the post. Example: `Write the release notes in Markdown.`. |
| `public` | number | yes | Use 1 to make the post public. Example: `1`. |
| `team` | number | yes | The owning ChangeCrab team ID. Example: `e.g. 101038`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "announced": true,
      "categories": [
        {}
      ],
      "created_at": "string",
      "creator": 1,
      "draft": true,
      "id": 1,
      "link": "https://example.com",
      "markdown": "string",
      "project": "string",
      "public": true,
      "publish_date": "string",
      "record": "string",
      "summary": "string",
      "team": 1,
      "type": "string",
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `announced` | boolean |  |
| `categories` | array<object> |  |
| `created_at` | string |  |
| `creator` | number |  |
| `draft` | boolean |  |
| `id` | number |  |
| `link` | string |  |
| `markdown` | string |  |
| `project` | string |  |
| `public` | boolean |  |
| `publish_date` | string |  |
| `record` | string |  |
| `summary` | string |  |
| `team` | number |  |
| `type` | string |  |
| `updated_at` | string |  |

## Native endpoint

Through the native ChangeCrab API, this operation is `PUT /changelogs/:id/posts/:postId` (base URL `https://changecrab.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-post.md) for the provider-specific parameters and requirements.

