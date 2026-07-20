# Simple Analytics: Export Data Points

Exports raw data points from Simple Analytics in JSON.

```
GET https://connect.mindcloud.co/v1/universal/simpleAnalytics/latest/actions/export-data-points
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Simple Analytics `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simpleAnalytics/latest/actions/export-data-points?connectionId=$CONNECTION_ID&hostname=Ava%20Chen&start=string&end=string&fields=string&type=string" \
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

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simpleAnalytics/latest/actions/export-data-points?${params}`, {
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
| `hostname` | string | yes | Website hostname to export data for, for example `simpleanalytics.com`. |
| `start` | string | yes | Start date in `YYYY-MM-DD` or `YYYY-MM-DDTHH` format. |
| `end` | string | yes | End date in `YYYY-MM-DD` or `YYYY-MM-DDTHH` format. |
| `fields` | string | yes | Comma-separated raw data fields to return, such as `added_iso,path`. |
| `type` | string | yes | Export data type, for example `pageviews`. |
| `timezone` | string | no | IANA time zone such as `Europe/Amsterdam`. |
| `robots` | boolean | no | Whether to include robot traffic in the export. Default: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "datapoints": [
        {}
      ],
      "meta": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `datapoints` | array<object> | Exported datapoints matching the requested filters. |
| `meta` | object | Export metadata including record count and generation timestamps. |

## Native endpoint

Through the native Simple Analytics API, this operation is `GET /api/export/datapoints` (base URL `https://simpleanalytics.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/export-data-points.md) for the provider-specific parameters and requirements.

