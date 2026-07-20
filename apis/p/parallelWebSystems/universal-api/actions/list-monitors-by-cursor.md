# Parallel Web Systems: List Monitors By Cursor



```
GET https://connect.mindcloud.co/v1/universal/parallelWebSystems/latest/actions/list-monitors-by-cursor
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Parallel Web Systems `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/parallelWebSystems/latest/actions/list-monitors-by-cursor?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/parallelWebSystems/latest/actions/list-monitors-by-cursor?${params}`, {
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
| `cursor` | string | no | Opaque pagination cursor returned by a previous list response. |
| `limit` | number | no | Maximum number of monitors to return. Default: `5`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
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
      },
      "next_cursor": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.cadence` | string | Monitor cadence. |
| `data.created_at` | date | Monitor creation timestamp. |
| `data.frequency` | string | Monitor frequency. |
| `data.include_backfill` | boolean | Whether backfill is included. |
| `data.last_run_at` | date | Timestamp of the last monitor run. |
| `data.monitor_id` | string | Parallel monitor identifier. |
| `data.query` | string | Monitor search query. |
| `data.status` | string | Monitor status. |
| `data.webhook.url` | string | Webhook destination URL. |
| `next_cursor` | string | Opaque pagination cursor for the next page. |

## Native endpoint

Through the native Parallel Web Systems API, this operation is `GET /v1alpha/monitors/list` (base URL `https://api.parallel.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-monitors-by-cursor.md) for the provider-specific parameters and requirements.

