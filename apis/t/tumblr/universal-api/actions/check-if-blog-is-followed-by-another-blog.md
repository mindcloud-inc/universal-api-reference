# Tumblr: Check If Blog Is Followed By Another Blog

Checks whether a Tumblr blog is followed by another blog.

```
GET https://connect.mindcloud.co/v1/universal/tumblr/latest/actions/check-if-blog-is-followed-by-another-blog
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tumblr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tumblr/latest/actions/check-if-blog-is-followed-by-another-blog?connectionId=$CONNECTION_ID&blogIdentifier=string&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "blogIdentifier": "string",
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tumblr/latest/actions/check-if-blog-is-followed-by-another-blog?${params}`, {
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
| `blogIdentifier` | string | yes | The blog that may be followed by another blog. |
| `query` | string | yes | The name of the blog that may be following your blog. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "followedBy": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `followedBy` | boolean |  |

## Native endpoint

Through the native Tumblr API, this operation is `GET /v2/blog/:blogIdentifier/followed_by` (base URL `https://api.tumblr.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-if-blog-is-followed-by-another-blog.md) for the provider-specific parameters and requirements.

