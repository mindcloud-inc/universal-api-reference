# Reka Vision: Move Videos To Group (V2)

Moves videos to a group in Reka Vision.

```
PUT https://connect.mindcloud.co/v1/universal/rekaVision/latest/actions/move-videos-to-group-v2
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reka Vision `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rekaVision/latest/actions/move-videos-to-group-v2" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "groupId": "string",
  "videoIds[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rekaVision/latest/actions/move-videos-to-group-v2', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "groupId": "string",
    "videoIds[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `groupId` | string | yes |  |
| `videoIds[]` | array<string> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "groupId": "string",
      "movedCount": 1,
      "status": "string",
      "videoIds": [
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
| `groupId` | string |  |
| `movedCount` | number |  |
| `status` | string |  |
| `videoIds` | array<string> |  |

## Native endpoint

Through the native Reka Vision API, this operation is `POST /v2/video-groups/:groupId/videos` (base URL `https://vision-agent.api.reka.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/move-videos-to-group-v2.md) for the provider-specific parameters and requirements.

