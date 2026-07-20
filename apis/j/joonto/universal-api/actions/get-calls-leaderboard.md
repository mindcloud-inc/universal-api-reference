# Joonto: Get Calls Leaderboard



```
GET https://connect.mindcloud.co/v1/universal/joonto/latest/actions/get-calls-leaderboard
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Joonto `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/joonto/latest/actions/get-calls-leaderboard?connectionId=$CONNECTION_ID&filter=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "filter": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/joonto/latest/actions/get-calls-leaderboard?${params}`, {
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
| `filter` | string | yes |  |
| `managers[]` | array<string> | no |  |
| `users[]` | array<string> | no |  |
| `callTypes[]` | array<string> | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Joonto API returns.

## Native endpoint

Through the native Joonto API, this operation is `POST /api/Live/Leaderboard/:filter` (base URL `https://api.joonto.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-calls-leaderboard.md) for the provider-specific parameters and requirements.

