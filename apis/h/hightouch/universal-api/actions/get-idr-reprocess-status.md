# Hightouch: Get IDR Reprocess Status

Retrieves IDR reprocessing status from Hightouch.

```
GET https://connect.mindcloud.co/v1/universal/hightouch/latest/actions/get-idr-reprocess-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Hightouch `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hightouch/latest/actions/get-idr-reprocess-status?connectionId=$CONNECTION_ID&graphId=string&requestId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "graphId": "string",
  "requestId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hightouch/latest/actions/get-idr-reprocess-status?${params}`, {
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
| `graphId` | string | yes | The IDR graph ID. |
| `requestId` | string | yes | The IDR reprocessing request ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error": "string",
      "queuedAt": "2026-05-07T12:00:00.000Z",
      "reprocessedAt": "2026-05-07T12:00:00.000Z",
      "reprocessedRunId": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error` | string | Error message, when available. |
| `queuedAt` | date | Queued timestamp. |
| `reprocessedAt` | date | Reprocessed timestamp. |
| `reprocessedRunId` | string | Run ID that reprocessed the identifiers. |
| `status` | string | Reprocessing request status. |

## Native endpoint

Through the native Hightouch API, this operation is `GET /idr/{graphId}/reprocess-status/{requestId}` (base URL `https://api.hightouch.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-idr-reprocess-status.md) for the provider-specific parameters and requirements.

