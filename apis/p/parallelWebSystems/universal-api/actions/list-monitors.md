# Parallel Web Systems: List Monitors



```
GET https://connect.mindcloud.co/v1/universal/parallelWebSystems/latest/actions/list-monitors
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Parallel Web Systems `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/parallelWebSystems/latest/actions/list-monitors?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/parallelWebSystems/latest/actions/list-monitors?${params}`, {
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
| `monitorId` | string | no | Monitor ID to start listing after. |
| `limit` | number | no | Maximum number of monitors to return. |

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

Through the native Parallel Web Systems API, this operation is `GET /v1alpha/monitors` (base URL `https://api.parallel.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-monitors.md) for the provider-specific parameters and requirements.

