# Simple Analytics: Export Hourly Data CSV

Exports hourly data from Simple Analytics in CSV.

```
GET https://connect.mindcloud.co/v1/universal/simpleAnalytics/latest/actions/export-hourly-data-csv
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Simple Analytics `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simpleAnalytics/latest/actions/export-hourly-data-csv?connectionId=$CONNECTION_ID&hostname=Ava%20Chen&start=string&end=string&fields=string&type=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "hostname": "Ava Chen",
  "start": "string",
  "end": "string",
  "fields": "string",
  "type": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simpleAnalytics/latest/actions/export-hourly-data-csv?${params}`, {
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
| `hostname` | string | yes |  |
| `start` | string | yes |  |
| `end` | string | yes |  |
| `fields` | string | yes |  |
| `type` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "csv": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `csv` | string | Raw CSV export body returned for the requested hourly window. |

## Native endpoint

Through the native Simple Analytics API, this operation is `GET /api/export/datapoints` (base URL `https://simpleanalytics.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/export-hourly-data-csv.md) for the provider-specific parameters and requirements.

