# Hippo Video: Generate Bulk Personalized Video Tracking IDs

Creates bulk personalized video tracking IDs in Hippo Video.

```
POST https://connect.mindcloud.co/v1/universal/hippoVideo/latest/actions/generate-bulk-personalized-video-tracking-ids
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hippo Video `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hippoVideo/latest/actions/generate-bulk-personalized-video-tracking-ids" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "videoId": 1,
  "file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hippoVideo/latest/actions/generate-bulk-personalized-video-tracking-ids', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "videoId": 1,
    "file": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `videoId` | number | yes | ID of the video |
| `file` | string | yes | Excel, CSV, or XLSX file with customer data |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "msg": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `msg` | string |  |

## Native endpoint

Through the native Hippo Video API, this operation is `POST /api/v1/me/video/bulk_personalize` (base URL `https://www.hippovideo.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-bulk-personalized-video-tracking-ids.md) for the provider-specific parameters and requirements.

