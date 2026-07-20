# CometAPI: Kling Identify Face

Identifies faces for Kling lip-sync in CometAPI.

```
POST https://connect.mindcloud.co/v1/universal/cometAPI/latest/actions/kling-identify-face
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CometAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cometAPI/latest/actions/kling-identify-face" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "videoUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cometAPI/latest/actions/kling-identify-face', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "videoUrl": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `videoUrl` | string | yes | Video URL for face identification. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "faces": [
        {}
      ],
      "status": "string",
      "task_id": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `faces` | array<object> |  |
| `status` | string |  |
| `task_id` | string |  |

## Native endpoint

Through the native CometAPI API, this operation is `POST /kling/v1/videos/identify-face` (base URL `https://api.cometapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/kling-identify-face.md) for the provider-specific parameters and requirements.

