# Process Plan: List Process Template Task Response Report Series Percent Grouped By Process Template Task Response for Process Template Task



```
GET https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/list-process-template-task-response-report-series-percent-grouped-by-process-template-task-response-for-process-template-task
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Process Plan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/list-process-template-task-response-report-series-percent-grouped-by-process-template-task-response-for-process-template-task?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/list-process-template-task-response-report-series-percent-grouped-by-process-template-task-response-for-process-template-task?${params}`, {
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
| `processTemplateTaskId` | string | no | Process template task ID. |

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
| `report_series_list[].series_value` | number |  |

## Native endpoint

Through the native Process Plan API, this operation is `GET /process_template_task/:processTemplateTaskId/process_template_response_report_series/list/percent/grouped_by/process_template_response` (base URL `https://apius0.processplan.com/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-process-template-task-response-report-series-percent-grouped-by-process-template-task-response-for-process-template-task.md) for the provider-specific parameters and requirements.

