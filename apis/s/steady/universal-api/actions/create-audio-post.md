# Steady: Create Audio Post

Creates a new audio post in Steady.

```
POST https://connect.mindcloud.co/v1/universal/steady/latest/actions/create-audio-post
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Steady `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/steady/latest/actions/create-audio-post" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "audioUrl": "https://example.com",
  "description": "string",
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/steady/latest/actions/create-audio-post', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "audioUrl": "https://example.com",
    "description": "string",
    "title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `audioUrl` | string | yes | A URL ending in .mp3 or .m4a. |
| `content` | string | no | Optional post content. HTML is sanitized by Steady. |
| `description` | string | yes | The description of the post. |
| `distributeAsEmail` | boolean | no | Optional boolean to send the post as email when published. |
| `distributeOnSteadyPage` | boolean | no | Optional boolean to display the post on the Steady page. |
| `publishAt` | date | no | Optional future ISO8601 datetime to schedule publication. |
| `publishedAt` | date | no | Optional ISO8601 datetime for an already-published post. |
| `restrictToPlanIds` | list<string> | no | Optional list of plan IDs that can access the post. |
| `teaserImage` | string | no | Optional image URL used when displaying the post on Steady. |
| `title` | string | yes | The title of the post. |

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

Through the native Steady API, this operation is `POST /posts/audio_posts` (base URL `https://steadyhq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-audio-post.md) for the provider-specific parameters and requirements.

