# UserVitals: Attach Item To Story

Attaches an idea or feedback item to a story.

```
PUT https://connect.mindcloud.co/v1/universal/userVitals/latest/actions/attach-item-to-story
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UserVitals `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/userVitals/latest/actions/attach-item-to-story" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "itemId": "string",
  "itemToken": "string",
  "parentId": "string",
  "roadmapId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/userVitals/latest/actions/attach-item-to-story', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "itemId": "string",
    "itemToken": "string",
    "parentId": "string",
    "roadmapId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `itemId` | string | yes | The feedback or idea id. |
| `itemToken` | string | yes | The feedback or idea token. |
| `parentId` | string | yes | The story id. |
| `roadmapId` | string | yes | The roadmap id. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native UserVitals API returns.

## Native endpoint

Through the native UserVitals API, this operation is `POST /stories/ideas` (base URL `https://app.roadmap.space/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/attach-item-to-story.md) for the provider-specific parameters and requirements.

