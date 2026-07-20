# Process Plan: List Process Instance Header Report Series Grouped By Started Day



```
GET https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/list-process-instance-header-report-series-grouped-by-started-day
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Process Plan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/list-process-instance-header-report-series-grouped-by-started-day?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/list-process-instance-header-report-series-grouped-by-started-day?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "report_series_list": [
        {
          "series_label": "2026-05-07T12:00:00.000Z",
          "series_value": 1
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `report_series_list[].series_label` | date |  |
| `report_series_list[].series_value` | number |  |

## Native endpoint

Through the native Process Plan API, this operation is `GET /process_instance_header_report_series/list/grouped_by/started_day` (base URL `https://apius0.processplan.com/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-process-instance-header-report-series-grouped-by-started-day.md) for the provider-specific parameters and requirements.

