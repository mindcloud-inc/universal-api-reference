# Process Plan: List Process Instance Header Report Series Pending Grouped By User for Process Template Group



```
GET https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/list-process-instance-header-report-series-pending-grouped-by-user-for-process-template-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Process Plan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/list-process-instance-header-report-series-pending-grouped-by-user-for-process-template-group?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/list-process-instance-header-report-series-pending-grouped-by-user-for-process-template-group?${params}`, {
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
| `processTemplateGroupId` | string | no | Process template group ID. |

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

Through the native Process Plan API, this operation is `GET /process_template_group/:processTemplateGroupId/process_instance_header_report_series/list/pending/grouped_by/user` (base URL `https://apius0.processplan.com/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-process-instance-header-report-series-pending-grouped-by-user-for-process-template-group.md) for the provider-specific parameters and requirements.

