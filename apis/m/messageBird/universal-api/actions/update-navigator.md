# MessageBird: Update Navigator



```
PUT https://connect.mindcloud.co/v1/universal/messageBird/latest/actions/update-navigator
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MessageBird `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/messageBird/latest/actions/update-navigator" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceId": "string",
  "navigatorId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/messageBird/latest/actions/update-navigator', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceId": "string",
    "navigatorId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspaceId` | string | yes | The Bird workspace ID that owns the navigator. |
| `navigatorId` | string | yes | The Bird navigator ID to update. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native MessageBird API returns.

## Native endpoint

Through the native MessageBird API, this operation is `PATCH /workspaces/:workspaceId/navigators/:navigatorId` (base URL `https://api.bird.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-navigator.md) for the provider-specific parameters and requirements.

