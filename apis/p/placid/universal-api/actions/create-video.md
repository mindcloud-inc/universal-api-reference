# Placid: Create Video

Creates a new video in Placid from template clips.

```
POST https://connect.mindcloud.co/v1/universal/placid/latest/actions/create-video
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Placid `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/placid/latest/actions/create-video" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/placid/latest/actions/create-video', {
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
| `webhookSuccess` | string | no |  |
| `passthrough` | string | no |  |
| `clips[]` | array<object> | no |  |
| `clips[].templateUuid` | string | no |  |
| `clips[].layers` | object | no |  |
| `transfer` | object | no |  |
| `modifications` | object | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "passthrough": "string",
      "pollingUrl": "https://example.com",
      "srtFiles": [
        {}
      ],
      "status": "string",
      "statusDisplay": "string",
      "transferUrl": "https://example.com",
      "type": "string",
      "videoUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `passthrough` | string |  |
| `pollingUrl` | string |  |
| `srtFiles` | array<object> |  |
| `status` | string |  |
| `statusDisplay` | string |  |
| `transferUrl` | string |  |
| `type` | string |  |
| `videoUrl` | string |  |

## Native endpoint

Through the native Placid API, this operation is `POST /api/rest/videos` (base URL `https://api.placid.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-video.md) for the provider-specific parameters and requirements.

