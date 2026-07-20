# Parallel Web Systems: Create Monitor



```
POST https://connect.mindcloud.co/v1/universal/parallelWebSystems/latest/actions/create-monitor
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Parallel Web Systems `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/parallelWebSystems/latest/actions/create-monitor" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/parallelWebSystems/latest/actions/create-monitor', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "cadence": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "frequency": "string",
      "include_backfill": true,
      "last_run_at": "2026-05-07T12:00:00.000Z",
      "monitor_id": "string",
      "query": "string",
      "status": "string",
      "webhook": {
        "url": "https://example.com"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `cadence` | string | Monitor cadence. |
| `created_at` | date | Monitor creation timestamp. |
| `frequency` | string | Monitor frequency. |
| `include_backfill` | boolean | Whether backfill is included. |
| `last_run_at` | date | Timestamp of the last monitor run. |
| `monitor_id` | string | Parallel monitor identifier. |
| `query` | string | Monitor search query. |
| `status` | string | Monitor status. |
| `webhook.url` | string | Webhook destination URL. |

## Native endpoint

Through the native Parallel Web Systems API, this operation is `POST /v1alpha/monitors` (base URL `https://api.parallel.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-monitor.md) for the provider-specific parameters and requirements.

