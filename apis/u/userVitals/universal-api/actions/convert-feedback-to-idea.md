# UserVitals: Convert Feedback To Idea

Converts a feedback item to an idea.

```
PUT https://connect.mindcloud.co/v1/universal/userVitals/latest/actions/convert-feedback-to-idea
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UserVitals `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/userVitals/latest/actions/convert-feedback-to-idea" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "feedbackId": "string",
  "feedbackToken": "string",
  "roadmapId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/userVitals/latest/actions/convert-feedback-to-idea', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "feedbackId": "string",
    "feedbackToken": "string",
    "roadmapId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `feedbackId` | string | yes | The feedback id. |
| `feedbackToken` | string | yes | The feedback token. |
| `roadmapId` | string | yes | The roadmap id. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native UserVitals API returns.

## Native endpoint

Through the native UserVitals API, this operation is `PUT /feedback/convert` (base URL `https://app.roadmap.space/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/convert-feedback-to-idea.md) for the provider-specific parameters and requirements.

