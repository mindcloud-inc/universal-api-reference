# Better Stack Uptime: Create Status Page

Creates a new status page in Better Stack Uptime.

```
POST https://connect.mindcloud.co/v1/universal/betterStackUptime/latest/actions/create-status-page
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Better Stack Uptime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/betterStackUptime/latest/actions/create-status-page" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "companyName": "Ava Chen",
  "companyUrl": "https://example.com",
  "subdomain": "string",
  "timezone": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/betterStackUptime/latest/actions/create-status-page', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "companyName": "Ava Chen",
    "companyUrl": "https://example.com",
    "subdomain": "string",
    "timezone": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `companyName` | string | yes | Status page company name. |
| `companyUrl` | string | yes | Public company URL shown on the status page. |
| `subdomain` | string | yes | Unique Better Stack status page subdomain. |
| `timezone` | string | yes | Status page timezone, for example UTC. |
| `automaticReports` | boolean | no | Enable automatic reports for the page. Default: `false`. |
| `subscribable` | boolean | no | Allow subscribers to opt into page updates. Default: `false`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Better Stack Uptime API returns.

## Native endpoint

Through the native Better Stack Uptime API, this operation is `POST /v2/status-pages` (base URL `https://uptime.betterstack.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-status-page.md) for the provider-specific parameters and requirements.

