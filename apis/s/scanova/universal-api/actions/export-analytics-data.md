# Scanova: Export Analytics Data



```
GET https://connect.mindcloud.co/v1/universal/scanova/latest/actions/export-analytics-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scanova `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scanova/latest/actions/export-analytics-data?connectionId=$CONNECTION_ID&from=2026-05-07T12%3A00%3A00.000Z&to=2026-05-07T12%3A00%3A00.000Z&fileFormat=string&filterBy=qrid&q%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "from": "2026-05-07T12:00:00.000Z",
  "to": "2026-05-07T12:00:00.000Z",
  "fileFormat": "string",
  "filterBy": "qrid",
  "q[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scanova/latest/actions/export-analytics-data?${params}`, {
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
| `from` | date | yes | Start date for analytics data (inclusive). Format: YYYY-MM-DD |
| `to` | date | yes | End date for analytics data (inclusive). Format: YYYY-MM-DD. Defaults to current date. |
| `fileFormat` | string | yes | Export file format |
| `filterBy` | list | yes | Filter by QR code ID or tags One of: `qrid`, `tags`. |
| `q[]` | array<string> | yes | Array of QR code IDs (if filter_by is 'qrid') or tags (if filter_by is 'tags') to include in the export |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Scanova API returns.

## Native endpoint

Through the native Scanova API, this operation is `POST /analytics/qr/export/` (base URL `https://management.scanova.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/export-analytics-data.md) for the provider-specific parameters and requirements.

