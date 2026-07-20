# Reka AI: Move Videos To Legacy Group

Updates legacy video group membership in Reka AI.

```
PUT https://connect.mindcloud.co/v1/universal/rekaAI/latest/actions/move-videos-to-legacy-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Reka AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/rekaAI/latest/actions/move-videos-to-legacy-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "video_ids": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rekaAI/latest/actions/move-videos-to-legacy-group', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "video_ids": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `video_ids` | string | yes | Video IDs to move |

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
| `groupId` | string | Destination group identifier |
| `movedCount` | number | Number of videos moved |
| `status` | string | Status of the move operation |
| `videoIds` | array<string> | Video IDs that were moved |

## Native endpoint

Through the native Reka AI API, this operation is `POST https://vision-agent.api.reka.ai/v1/videos/group` (base URL `https://api.reka.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/move-videos-to-legacy-group.md) for the provider-specific parameters and requirements.

