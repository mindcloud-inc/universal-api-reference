# MessageBird: Get Navigator Coverage



```
GET https://connect.mindcloud.co/v1/universal/messageBird/latest/actions/get-navigator-coverage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MessageBird `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/messageBird/latest/actions/get-navigator-coverage?connectionId=$CONNECTION_ID&workspaceId=string&navigatorId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "string",
  "navigatorId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/messageBird/latest/actions/get-navigator-coverage?${params}`, {
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
| `workspaceId` | string | yes | The Bird workspace ID that owns the navigator. |
| `navigatorId` | string | yes | The Bird navigator ID whose coverage should be retrieved. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native MessageBird API returns.

## Native endpoint

Through the native MessageBird API, this operation is `GET /workspaces/:workspaceId/navigators/:navigatorId/coverage` (base URL `https://api.bird.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-navigator-coverage.md) for the provider-specific parameters and requirements.

