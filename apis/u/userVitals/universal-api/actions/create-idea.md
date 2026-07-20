# UserVitals: Create Idea

Creates a new idea in the roadmap API.

```
POST https://connect.mindcloud.co/v1/universal/userVitals/latest/actions/create-idea
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UserVitals `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/userVitals/latest/actions/create-idea" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "roadmapId": "string",
  "title": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/userVitals/latest/actions/create-idea', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "roadmapId": "string",
    "title": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `category` | string | no | The idea category. |
| `description` | string | no | The idea description. |
| `roadmapId` | string | yes | The roadmap id. |
| `title` | string | yes | The idea title. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native UserVitals API returns.

## Native endpoint

Through the native UserVitals API, this operation is `POST /ideas` (base URL `https://app.roadmap.space/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-idea.md) for the provider-specific parameters and requirements.

