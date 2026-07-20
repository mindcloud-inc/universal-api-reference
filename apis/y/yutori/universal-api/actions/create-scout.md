# Yutori: Create Scout

Creates a new scout in Yutori.

```
POST https://connect.mindcloud.co/v1/universal/yutori/latest/actions/create-scout
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Yutori `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/yutori/latest/actions/create-scout" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "query": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/yutori/latest/actions/create-scout', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "query": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `query` | string | yes | What the scout should monitor in natural language. |
| `outputInterval` | number | no | How often to run the scout, in seconds. |
| `startTimestamp` | number | no | Unix timestamp for when the scout should start. |
| `userTimezone` | string | no | Timezone used for scheduling context. |
| `userLocation` | string | no | Coarse user location such as city, region, country. |
| `outputSchema` | object | no | Optional JSON Schema for structured scout output. |
| `skipEmail` | boolean | no | If true, skip email notifications. |
| `webhookUrl` | string | no | Webhook URL to receive scout updates. |
| `webhookFormat` | string | no | Webhook payload format. |
| `isPublic` | boolean | no | Whether the scout is publicly accessible. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Yutori API returns.

## Native endpoint

Through the native Yutori API, this operation is `POST /v1/scouting/tasks` (base URL `https://api.yutori.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-scout.md) for the provider-specific parameters and requirements.

