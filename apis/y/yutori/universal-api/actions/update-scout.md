# Yutori: Update Scout

Updates an existing scout in Yutori.

```
PUT https://connect.mindcloud.co/v1/universal/yutori/latest/actions/update-scout
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Yutori `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/yutori/latest/actions/update-scout" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "scoutId": "string",
  "query": "string",
  "queryObject": {},
  "userTimezone": "string",
  "llmOutput": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/yutori/latest/actions/update-scout', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "scoutId": "string",
    "query": "string",
    "queryObject": {},
    "userTimezone": "string",
    "llmOutput": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `scoutId` | string | yes | The scout UUID. |
| `query` | string | yes |  |
| `queryObject` | object | yes |  |
| `displayName` | string | no |  |
| `userTimezone` | string | yes |  |
| `llmOutput` | object | yes |  |
| `outputInterval` | number | no |  |
| `nextOutputTimestamp` | number | no |  |
| `userLocation` | string | no |  |
| `isPublic` | boolean | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Yutori API returns.

## Native endpoint

Through the native Yutori API, this operation is `PUT /v1/scouting/tasks/:scout_id` (base URL `https://api.yutori.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-scout.md) for the provider-specific parameters and requirements.

