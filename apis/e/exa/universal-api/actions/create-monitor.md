# Exa: Create Monitor

Creates a new monitor in Exa.

```
POST https://connect.mindcloud.co/v1/universal/exa/latest/actions/create-monitor
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Exa `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/exa/latest/actions/create-monitor" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "search.query": "string",
  "webhook.url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/exa/latest/actions/create-monitor', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "search.query": "string",
    "webhook.url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `metadata` | object | no | Optional key-value metadata object. |
| `name` | string | no | Optional display name for the monitor. |
| `outputSchema` | object | no | Optional JSON schema for structured monitor output. |
| `search.contents` | object | no | Optional content extraction configuration object. |
| `search.numResults` | number | no | Number of results to retrieve per run. |
| `search.query` | string | yes | Search query to run on every monitor execution. |
| `trigger.period` | string | no | Interval duration like 1h, 6h, 1d, or 7d. |
| `trigger.type` | string | no | Use interval when scheduling the monitor. |
| `webhook.events[]` | array<string> | no | Optional list of monitor events to deliver. |
| `webhook.url` | string | yes | HTTPS URL that receives monitor events. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "metadata": {},
      "name": "Ava Chen",
      "nextRunAt": "2026-05-07T12:00:00.000Z",
      "outputSchema": {},
      "search": {},
      "status": "string",
      "trigger": {},
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "webhook": {},
      "webhookSecret": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | Creation timestamp. |
| `id` | string | Unique monitor identifier. |
| `metadata` | object | Custom metadata. |
| `name` | string | Monitor display name. |
| `nextRunAt` | date | Next scheduled run timestamp. |
| `outputSchema` | object | Structured output schema configuration. |
| `search` | object | Search configuration. |
| `status` | string | Monitor status. |
| `trigger` | object | Interval trigger configuration. |
| `updatedAt` | date | Last update timestamp. |
| `webhook` | object | Webhook configuration. |
| `webhookSecret` | string | One-time webhook signing secret returned only on creation. |

## Native endpoint

Through the native Exa API, this operation is `POST /monitors` (base URL `https://api.exa.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-monitor.md) for the provider-specific parameters and requirements.

