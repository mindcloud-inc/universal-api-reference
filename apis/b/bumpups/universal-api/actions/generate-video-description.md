# Bumpups: Generate Video Description

Creates a video description in Bumpups.

```
POST https://connect.mindcloud.co/v1/universal/bumpups/latest/actions/generate-video-description
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bumpups `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bumpups/latest/actions/generate-video-description" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bumpups/latest/actions/generate-video-description', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `url` | string | yes | The YouTube video URL to analyze. |
| `language` | string | no | The two-letter language code for the response. Default: `en`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "language": "string",
      "model": "string",
      "url": "https://example.com",
      "videoDuration": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `language` | string |  |
| `model` | string |  |
| `url` | string |  |
| `videoDuration` | number |  |

## Native endpoint

Through the native Bumpups API, this operation is `POST /creator/description` (base URL `https://api.bumpups.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-video-description.md) for the provider-specific parameters and requirements.

