# Vimeo: Add Video to Project

Adds a video to a project in Vimeo.

```
POST https://connect.mindcloud.co/v1/universal/vimeo/latest/actions/add-video-to-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Vimeo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/vimeo/latest/actions/add-video-to-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "userId": "152184",
  "projectId": "12345",
  "videoId": "33031367"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vimeo/latest/actions/add-video-to-project', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "userId": "152184",
    "projectId": "12345",
    "videoId": "33031367"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `userId` | number | yes | The ID of the user. Example: `152184`. |
| `projectId` | number | yes | The ID of the folder. Example: `12345`. |
| `videoId` | number | yes | The ID of the video. Example: `33031367`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `value` | string | The raw response body. Vimeo returns an empty string on successful 204 No Content mutations. |

## Native endpoint

Through the native Vimeo API, this operation is `PUT /users/:user_id/projects/:project_id/videos/:video_id` (base URL `https://api.vimeo.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-video-to-project.md) for the provider-specific parameters and requirements.

