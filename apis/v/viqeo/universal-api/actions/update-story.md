# Viqeo: Update Story

Updates an existing story in Viqeo.

```
PUT https://connect.mindcloud.co/v1/universal/viqeo/latest/actions/update-story
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Viqeo `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/viqeo/latest/actions/update-story" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": "string",
  "storyId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/viqeo/latest/actions/update-story', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": "string",
    "storyId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `projectId` | string | yes | Project identifier from the path. |
| `storyId` | string | yes | Story identifier from the path. |
| `title` | string | no | Optional story title. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Viqeo API returns.

## Native endpoint

Through the native Viqeo API, this operation is `POST /media-platform/v1/project/:projectId/story/:storyId` (base URL `https://api.viqeo.tv`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-story.md) for the provider-specific parameters and requirements.

