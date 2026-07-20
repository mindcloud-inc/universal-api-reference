# Late: Create Post



```
POST https://connect.mindcloud.co/v1/universal/late/latest/actions/create-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Late `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/late/latest/actions/create-post" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/late/latest/actions/create-post', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | no |  |
| `content` | string | no | Post caption/text for the draft seed post. |
| `isDraft` | boolean | no | Hidden default to force deterministic draft creation for verification setup. Default: `true`. |
| `scheduledFor` | string | no |  |
| `publishNow` | boolean | no |  |
| `timezone` | string | no |  |
| `queuedFromProfile` | string | no |  |
| `queueId` | string | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `mediaItems[]` | array<object> | no |  |
| `platforms[]` | array<object> | no |  |
| `tags[]` | array<string> | no |  |
| `hashtags[]` | array<string> | no |  |
| `mentions[]` | array<string> | no |  |
| `crosspostingEnabled` | boolean | no |  |
| `metadata` | object | no |  |
| `tiktokSettings` | object | no |  |
| `recycling` | object | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string",
      "post": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Provider success message. |
| `post` | object | Created post payload. |

## Native endpoint

Through the native Late API, this operation is `POST /posts` (base URL `https://zernio.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-post.md) for the provider-specific parameters and requirements.

