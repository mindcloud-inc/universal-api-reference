# Raven Tools: Decline Link

Updates a link to declined in Raven Tools.

```
PUT https://connect.mindcloud.co/v1/universal/ravenTools/latest/actions/decline-link
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Raven Tools `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/ravenTools/latest/actions/decline-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "link": "JSON array with one Raven link record including link id and status set to declined."
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ravenTools/latest/actions/decline-link', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "link": "JSON array with one Raven link record including link id and status set to declined."
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `link` | string | yes | Default: `[{"status":"declined","link id":"31311500"}]`. Example: `JSON array with one Raven link record including link id and status set to declined.`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Raven Tools API returns.

## Native endpoint

Through the native Raven Tools API, this operation is `GET /api` (base URL `https://api.raventools.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/decline-link.md) for the provider-specific parameters and requirements.

