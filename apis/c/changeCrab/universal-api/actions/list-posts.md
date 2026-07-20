# ChangeCrab: List Posts

Retrieves posts for a changelog from ChangeCrab.

```
GET https://connect.mindcloud.co/v1/universal/changeCrab/latest/actions/list-posts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ChangeCrab `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/changeCrab/latest/actions/list-posts?connectionId=$CONNECTION_ID&id=e.g.%20product-updates" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "e.g. product-updates"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/changeCrab/latest/actions/list-posts?${params}`, {
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
| `id` | string | yes | The ChangeCrab changelog access ID. Example: `e.g. product-updates`. |

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

Through the native ChangeCrab API, this operation is `GET /changelogs/:id/posts` (base URL `https://changecrab.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-posts.md) for the provider-specific parameters and requirements.

