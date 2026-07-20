# CallRail: Summarize Call Data By Time Series

Retrieves call time-series summary data from CallRail.

```
GET https://connect.mindcloud.co/v1/universal/callRail/latest/actions/summarize-call-data-by-time-series
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CallRail `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/callRail/latest/actions/summarize-call-data-by-time-series?connectionId=$CONNECTION_ID&account_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "account_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/callRail/latest/actions/summarize-call-data-by-time-series?${params}`, {
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
| `account_id` | string | yes | The CallRail account ID. |
| `company_id` | string | no | Limit the time series to one company. |
| `fields` | string | no | Comma-separated time-series fields to include. |
| `interval` | string | no | Time bucket size such as day, week, or month. |
| `date_range` | string | no | Standard CallRail date range filter. |
| `start_date` | string | no | Start of a custom date range in ISO 8601 format. |
| `end_date` | string | no | End of a custom date range in ISO 8601 format. |
| `time_zone` | string | no | Time zone for grouping the time series. |
| `device` | string | no | Filter the time series by caller device type. |
| `tags` | string | no | Comma-separated tag names to match. |
| `direction` | string | no | Filter by inbound or outbound calls. |
| `answer_status` | string | no | Filter by whether calls were answered or missed. |
| `first_time_callers` | boolean | no | Restrict results to first-time callers when true. |
| `lead_status` | string | no | Filter results by lead status. |
| `min_duration` | number | no | Minimum call duration in seconds. |
| `max_duration` | number | no | Maximum call duration in seconds. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "date": "string",
          "key": "string",
          "totalCalls": 1
        }
      ],
      "endDate": "string",
      "startDate": "string",
      "timeZone": "string",
      "totalResults": {
        "totalCalls": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `data[].date` | string |  |
| `data[].key` | string |  |
| `data[].totalCalls` | number |  |
| `endDate` | string |  |
| `startDate` | string |  |
| `timeZone` | string |  |
| `totalResults` | object |  |
| `totalResults.totalCalls` | number |  |

## Native endpoint

Through the native CallRail API, this operation is `GET /v3/a/:account_id/calls/timeseries.json` (base URL `https://api.callrail.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/summarize-call-data-by-time-series.md) for the provider-specific parameters and requirements.

