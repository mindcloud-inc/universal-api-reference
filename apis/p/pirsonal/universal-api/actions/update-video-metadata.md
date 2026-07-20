# Pirsonal: Update Video Metadata

Updates metadata for an existing video in Pirsonal.

```
PUT https://connect.mindcloud.co/v1/universal/pirsonal/latest/actions/update-video-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pirsonal `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pirsonal/latest/actions/update-video-metadata" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "videoID": "string",
  "metaData": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pirsonal/latest/actions/update-video-metadata', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "videoID": "string",
    "metaData": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `videoID` | string | yes | ID of the video whose metadata should be updated. |
| `metaData` | object | yes | VideoMetaData_t object with updated metadata. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string | Pirsonal metadata update response, normally OK. |

## Native endpoint

Through the native Pirsonal API, this operation is `POST /api` (base URL `https://app.pirsonal.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-video-metadata.md) for the provider-specific parameters and requirements.

