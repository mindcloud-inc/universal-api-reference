# Honeybadger: Ping Check-in

Reports a check-in to Honeybadger by ID.

```
POST https://connect.mindcloud.co/v1/universal/honeybadger/latest/actions/ping-check-in
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Honeybadger `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/honeybadger/latest/actions/ping-check-in" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "checkInId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/honeybadger/latest/actions/ping-check-in', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "checkInId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `checkInId` | string | yes | The case-sensitive check-in endpoint ID from Honeybadger. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Honeybadger API returns.

## Native endpoint

Through the native Honeybadger API, this operation is `GET /check_in/:checkInId` (base URL `https://api.honeybadger.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/ping-check-in.md) for the provider-specific parameters and requirements.

