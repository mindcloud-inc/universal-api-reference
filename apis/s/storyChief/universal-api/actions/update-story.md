# StoryChief: Update Story

Updates an existing story in StoryChief.

```
PUT https://connect.mindcloud.co/v1/universal/storyChief/latest/actions/update-story
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a StoryChief `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/storyChief/latest/actions/update-story" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "storyId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/storyChief/latest/actions/update-story', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "storyId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `authorId` | string | no | Updated author ID for the story. |
| `content` | string | no | Updated story HTML content. |
| `excerpt` | string | no | Updated story excerpt. |
| `slug` | string | no | Updated story slug. |
| `storyId` | number | yes | Story identifier from the path. |
| `title` | string | no | Updated story title. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native StoryChief API returns.

## Native endpoint

Through the native StoryChief API, this operation is `PUT /stories/:storyId` (base URL `https://api.storychief.io/1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-story.md) for the provider-specific parameters and requirements.

