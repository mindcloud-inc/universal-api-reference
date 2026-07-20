# Bumpups: Staging Recommendations

Creates staging recommendations from a video in Bumpups.

```
POST https://connect.mindcloud.co/v1/universal/bumpups/latest/actions/staging-recommendations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bumpups `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bumpups/latest/actions/staging-recommendations" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bumpups/latest/actions/staging-recommendations', {
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
| `outputFormat` | string | no | The desired output format. Default: `text`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "language": "string",
      "model": "string",
      "output": "string",
      "outputFormat": "string",
      "prompt": "string",
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
| `language` | string |  |
| `model` | string |  |
| `output` | string |  |
| `outputFormat` | string |  |
| `prompt` | string |  |
| `url` | string |  |
| `videoDuration` | number |  |

## Native endpoint

Through the native Bumpups API, this operation is `POST /chat` (base URL `https://api.bumpups.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/staging-recommendations.md) for the provider-specific parameters and requirements.

