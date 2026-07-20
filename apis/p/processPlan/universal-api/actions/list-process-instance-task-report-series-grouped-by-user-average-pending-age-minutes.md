# Process Plan: List Process Instance Task Report Series Grouped By User Average Pending Age Minutes



```
GET https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/list-process-instance-task-report-series-grouped-by-user-average-pending-age-minutes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Process Plan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/list-process-instance-task-report-series-grouped-by-user-average-pending-age-minutes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/list-process-instance-task-report-series-grouped-by-user-average-pending-age-minutes?${params}`, {
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
          "series_id": "string",
          "series_label": "string",
          "series_unit": "string",
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
| `report_series_list[].series_id` | string |  |
| `report_series_list[].series_label` | string |  |
| `report_series_list[].series_unit` | string |  |
| `report_series_list[].series_value` | number |  |

## Native endpoint

Through the native Process Plan API, this operation is `GET /process_instance_task_report_series/list/grouped_by_user_average/pending_age_minutes` (base URL `https://apius0.processplan.com/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-process-instance-task-report-series-grouped-by-user-average-pending-age-minutes.md) for the provider-specific parameters and requirements.

