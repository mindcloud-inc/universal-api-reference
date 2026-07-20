# Reka AI: Quick Tag Video

Creates quick tags for a video in Reka AI.

```
POST https://connect.mindcloud.co/v1/universal/rekaAI/latest/actions/quick-tag-video
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reka AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rekaAI/latest/actions/quick-tag-video" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rekaAI/latest/actions/quick-tag-video', {
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



## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "status": "string",
      "tags": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Related identifier. |
| `status` | string | Processing status. |
| `tags` | array<string> | Generated tags. |

## Native endpoint

Through the native Reka AI API, this operation is `POST https://vision-agent.api.reka.ai/v1/qa/quicktag` (base URL `https://api.reka.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/quick-tag-video.md) for the provider-specific parameters and requirements.

