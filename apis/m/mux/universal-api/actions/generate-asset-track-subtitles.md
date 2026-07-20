# Mux: Generate Asset Track Subtitles



```
POST https://connect.mindcloud.co/v1/universal/mux/latest/actions/generate-asset-track-subtitles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mux `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mux/latest/actions/generate-asset-track-subtitles" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "assetId": "string",
  "generatedSubtitles[]": [
    {}
  ],
  "trackId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mux/latest/actions/generate-asset-track-subtitles', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "assetId": "string",
    "generatedSubtitles[]": [{}],
    "trackId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `assetId` | string | yes | The Mux asset ID. |
| `generatedSubtitles[]` | array<object> | yes | Generated subtitle definitions. |
| `trackId` | string | yes | The Mux track ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
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
| `data` | array<object> |  |

## Native endpoint

Through the native Mux API, this operation is `POST /video/v1/assets/{ASSET_ID}/tracks/{TRACK_ID}/generate-subtitles` (base URL `https://api.mux.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-asset-track-subtitles.md) for the provider-specific parameters and requirements.

