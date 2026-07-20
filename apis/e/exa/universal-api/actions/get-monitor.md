# Exa: Get Monitor

Retrieves a monitor from Exa.

```
GET https://connect.mindcloud.co/v1/universal/exa/latest/actions/get-monitor
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Exa `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/exa/latest/actions/get-monitor?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/exa/latest/actions/get-monitor?${params}`, {
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
| `id` | string | yes | Monitor identifier. |

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

Through the native Exa API, this operation is `GET /monitors/:id` (base URL `https://api.exa.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-monitor.md) for the provider-specific parameters and requirements.

