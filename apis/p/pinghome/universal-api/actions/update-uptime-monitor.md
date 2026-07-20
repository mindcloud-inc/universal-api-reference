# Pinghome: Update Uptime Monitor

Updates an existing uptime monitor in Pinghome.

```
PUT https://connect.mindcloud.co/v1/universal/pinghome/latest/actions/update-uptime-monitor
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinghome `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pinghome/latest/actions/update-uptime-monitor" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "name": "Ava Chen",
  "method": "string",
  "serviceId": "string",
  "url": "https://example.com",
  "regions[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pinghome/latest/actions/update-uptime-monitor', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "name": "Ava Chen",
    "method": "string",
    "serviceId": "string",
    "url": "https://example.com",
    "regions[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The unique ID of the uptime monitor. |
| `name` | string | yes | The name of the uptime resource. |
| `isAdvanced` | boolean | no | Whether the resource uses advanced monitoring options. |
| `method` | string | yes | The HTTP method used for uptime checks. |
| `gracePeriod` | number | no | Grace period before considering a failure. |
| `recoveryPeriod` | number | no | Recovery period before considering the resource recovered. |
| `skipSslError` | boolean | no | Whether SSL errors should be skipped. |
| `notFollowRedirect` | boolean | no | Whether redirects should not be followed. |
| `serviceId` | string | yes | The service associated with the monitor. |
| `url` | string | yes | The target URL to monitor. |
| `regions[]` | array<string> | yes | Regions used to run the uptime checks. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Pinghome API returns.

## Native endpoint

Through the native Pinghome API, this operation is `PUT /resource-cmd/v1/resource/:id` (base URL `https://api.pinghome.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-uptime-monitor.md) for the provider-specific parameters and requirements.

