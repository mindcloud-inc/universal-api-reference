# Exa: Update Monitor

Updates an existing monitor in Exa.

```
PUT https://connect.mindcloud.co/v1/universal/exa/latest/actions/update-monitor
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Exa `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/exa/latest/actions/update-monitor" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/exa/latest/actions/update-monitor', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Monitor identifier. |
| `metadata` | object | no | Updated metadata object. |
| `name` | string | no | Updated monitor name. |
| `outputSchema` | object | no | Updated JSON schema for structured output. |
| `search.contents` | object | no | Updated content extraction configuration object. |
| `search.numResults` | number | no | Updated result count per run. |
| `search.query` | string | no | Updated search query. |
| `status` | string | no | Monitor status: active or paused. |
| `trigger.period` | string | no | Updated interval duration. |
| `trigger.type` | string | no | Use interval when scheduling the monitor. |
| `webhook.events[]` | array<string> | no | Updated list of webhook events. |
| `webhook.url` | string | no | Updated HTTPS webhook URL. |

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
      "webhook": {}
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

## Native endpoint

Through the native Exa API, this operation is `PATCH /monitors/:id` (base URL `https://api.exa.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-monitor.md) for the provider-specific parameters and requirements.

