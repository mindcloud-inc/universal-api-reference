# Steady: Update Audio Post

Updates an existing audio post in Steady.

```
PUT https://connect.mindcloud.co/v1/universal/steady/latest/actions/update-audio-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Steady `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/steady/latest/actions/update-audio-post" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "postId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/steady/latest/actions/update-audio-post', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "postId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `audioUrl` | string | no | A URL ending in .mp3 or .m4a. |
| `content` | string | no | Optional post content. HTML is sanitized by Steady. |
| `description` | string | no | The description of the post. |
| `distributeAsEmail` | boolean | no | Optional boolean to send the post as email when published. |
| `distributeOnSteadyPage` | boolean | no | Optional boolean to display the post on the Steady page. |
| `postId` | string | yes | The ID of the audio post to update. |
| `publishAt` | date | no | Optional future ISO8601 datetime to schedule publication when the post is not yet published. |
| `restrictToPlanIds` | list<string> | no | Optional list of plan IDs that can access the post. |
| `teaserImage` | string | no | Optional image URL used when displaying the post on Steady. |
| `title` | string | no | The title of the post. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "attributes": {
          "content": "string",
          "description": "string",
          "restricted": true,
          "title": "string"
        },
        "id": "string",
        "type": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.attributes.content` | string |  |
| `data.attributes.description` | string |  |
| `data.attributes.restricted` | boolean |  |
| `data.attributes.title` | string |  |
| `data.id` | string |  |
| `data.type` | string |  |

## Native endpoint

Through the native Steady API, this operation is `PUT /posts/audio_posts/:post_id` (base URL `https://steadyhq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-audio-post.md) for the provider-specific parameters and requirements.

