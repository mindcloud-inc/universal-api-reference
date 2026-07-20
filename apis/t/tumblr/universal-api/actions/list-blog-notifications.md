# Tumblr: List Blog Notifications

Retrieves activity notifications for a Tumblr blog.

```
GET https://connect.mindcloud.co/v1/universal/tumblr/latest/actions/list-blog-notifications
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tumblr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tumblr/latest/actions/list-blog-notifications?connectionId=$CONNECTION_ID&blogIdentifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "blogIdentifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tumblr/latest/actions/list-blog-notifications?${params}`, {
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
| `blogIdentifier` | string | yes | The blog whose activity feed should be retrieved. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `before` | number | no | Unix epoch timestamp that begins the page. |
| `types` | list<string> | no | One or more notification types to filter by. Accepts multiple values as an array. |
| `rollups` | boolean | no | Whether to roll up similar activity items into single items. Default: `true`. |
| `omitPostIds` | list<string> | no | One or more of your own post IDs to filter out. Accepts multiple values as an array. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "notifications": [
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
| `notifications` | array<object> |  |

## Native endpoint

Through the native Tumblr API, this operation is `GET /v2/blog/:blogIdentifier/notifications` (base URL `https://api.tumblr.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-blog-notifications.md) for the provider-specific parameters and requirements.

