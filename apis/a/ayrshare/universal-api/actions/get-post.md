# Ayrshare: Get Post

Retrieves a post by Ayrshare post ID.

```
GET https://connect.mindcloud.co/v1/universal/ayrshare/latest/actions/get-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ayrshare `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ayrshare/latest/actions/get-post?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ayrshare/latest/actions/get-post?${params}`, {
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
| `id` | string | yes | Ayrshare Post ID returned by the publish post endpoint. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "2026-05-07T12:00:00.000Z",
      "errors": [
        {}
      ],
      "id": "string",
      "platforms": [
        "string"
      ],
      "post": "string",
      "postIds": [
        {}
      ],
      "scheduleDate": "2026-05-07T12:00:00.000Z",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | date | Creation timestamp. |
| `errors` | array<object> | Errors returned for the post. |
| `id` | string | Ayrshare Post ID. |
| `platforms` | array<string> | Platforms associated with the post. |
| `post` | string | Post text. |
| `postIds` | array<object> | Social-network-specific post IDs. |
| `scheduleDate` | date | Post schedule or publish timestamp. |
| `status` | string | Post status. |

## Native endpoint

Through the native Ayrshare API, this operation is `GET /post/:id` (base URL `https://api.ayrshare.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-post.md) for the provider-specific parameters and requirements.

