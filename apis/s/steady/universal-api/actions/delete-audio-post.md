# Steady: Delete Audio Post

Deletes an existing audio post from Steady.

```
DELETE https://connect.mindcloud.co/v1/universal/steady/latest/actions/delete-audio-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Steady `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/steady/latest/actions/delete-audio-post?connectionId=$CONNECTION_ID&postId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "postId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/steady/latest/actions/delete-audio-post?${params}`, {
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
| `postId` | string | yes | The ID of the audio post to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "id": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.id` | string |  |

## Native endpoint

Through the native Steady API, this operation is `DELETE /posts/audio_posts/:post_id` (base URL `https://steadyhq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-audio-post.md) for the provider-specific parameters and requirements.

