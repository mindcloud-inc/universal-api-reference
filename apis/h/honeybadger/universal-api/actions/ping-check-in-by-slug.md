# Honeybadger: Ping Check-in by Slug

Reports a check-in to Honeybadger by slug.

```
POST https://connect.mindcloud.co/v1/universal/honeybadger/latest/actions/ping-check-in-by-slug
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Honeybadger `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/honeybadger/latest/actions/ping-check-in-by-slug" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "checkInSlug": "daily-reports"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/honeybadger/latest/actions/ping-check-in-by-slug', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "checkInSlug": "daily-reports"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `checkInSlug` | string | yes | Slug identifier configured on the Honeybadger check-in. Example: `daily-reports`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Honeybadger API returns.

## Native endpoint

Through the native Honeybadger API, this operation is `GET /check_in/:apiKey/:checkInSlug` (base URL `https://api.honeybadger.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/ping-check-in-by-slug.md) for the provider-specific parameters and requirements.

