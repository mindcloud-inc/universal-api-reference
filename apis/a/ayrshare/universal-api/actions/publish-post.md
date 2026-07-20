# Ayrshare: Publish Post

Publishes a post to social networks with Ayrshare.

```
POST https://connect.mindcloud.co/v1/universal/ayrshare/latest/actions/publish-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ayrshare `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ayrshare/latest/actions/publish-post" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "post": "string",
  "platforms[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ayrshare/latest/actions/publish-post', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "post": "string",
    "platforms[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `post` | string | yes | Text to publish to the selected social platforms. |
| `platforms[]` | array<string> | yes | Social platforms to publish to. Ayrshare values include twitter, facebook, instagram, linkedin, youtube, tiktok, and all. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `mediaUrls[]` | array<string> | no | HTTPS image or video URLs to attach to the post. |
| `scheduleDate` | date | no | UTC ISO 8601 date and time to schedule the post. |
| `randomPost` | boolean | no | Generate random post text for testing instead of using Post Text. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "errors": [
        {}
      ],
      "id": "string",
      "postIds": [
        {}
      ],
      "refId": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `errors` | array<object> | Per-platform or request errors. |
| `id` | string | Ayrshare Post ID. |
| `postIds` | array<object> | Per-platform publish results. |
| `refId` | string | Ayrshare profile reference ID. |
| `status` | string | Ayrshare publish status. |

## Native endpoint

Through the native Ayrshare API, this operation is `POST /post` (base URL `https://api.ayrshare.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/publish-post.md) for the provider-specific parameters and requirements.

