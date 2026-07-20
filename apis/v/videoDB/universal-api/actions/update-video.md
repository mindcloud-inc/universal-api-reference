# VideoDB: Update Video

Updates an existing video in VideoDB.

```
PUT https://connect.mindcloud.co/v1/universal/videoDB/latest/actions/update-video
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a VideoDB `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/videoDB/latest/actions/update-video" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "videoId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/videoDB/latest/actions/update-video', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "videoId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `videoId` | string | yes | Video ID |
| `name` | string | no | Updated video name |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `name` | string |  |

## Native endpoint

Through the native VideoDB API, this operation is `PATCH /video/:video_id` (base URL `https://api.videodb.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-video.md) for the provider-specific parameters and requirements.

