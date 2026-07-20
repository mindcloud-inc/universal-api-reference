# UserVitals: Move Idea

Moves an idea to another roadmap state.

```
PUT https://connect.mindcloud.co/v1/universal/userVitals/latest/actions/move-idea
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UserVitals `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/userVitals/latest/actions/move-idea" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "ideaId": "string",
  "ideaToken": "string",
  "roadmapId": "string",
  "targetState": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/userVitals/latest/actions/move-idea', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "ideaId": "string",
    "ideaToken": "string",
    "roadmapId": "string",
    "targetState": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `ideaId` | string | yes | The idea id. |
| `ideaToken` | string | yes | The idea token. |
| `roadmapId` | string | yes | The roadmap id. |
| `targetState` | string | yes | The destination state: widget, idea, or active. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native UserVitals API returns.

## Native endpoint

Through the native UserVitals API, this operation is `POST /ideas/move/:type` (base URL `https://app.roadmap.space/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/move-idea.md) for the provider-specific parameters and requirements.

