# Colossyan: Delete Generated Video

Deletes a generated video from Colossyan.

```
DELETE https://connect.mindcloud.co/v1/universal/colossyan/latest/actions/delete-generated-video
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Colossyan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/colossyan/latest/actions/delete-generated-video?connectionId=$CONNECTION_ID&videoId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "videoId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/colossyan/latest/actions/delete-generated-video?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `videoId` | string | yes | ID of the generated video to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | string | Deletion confirmation message from Colossyan. |

## Native endpoint

Through the native Colossyan API, this operation is `DELETE /generated-videos/:videoId` (base URL `https://app.colossyan.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-generated-video.md) for the provider-specific parameters and requirements.

