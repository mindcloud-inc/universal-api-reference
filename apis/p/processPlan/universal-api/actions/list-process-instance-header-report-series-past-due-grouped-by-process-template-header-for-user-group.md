# Process Plan: List Process Instance Header Report Series Past Due Grouped By Process Template Header for User Group



```
GET https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/list-process-instance-header-report-series-past-due-grouped-by-process-template-header-for-user-group
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Process Plan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/list-process-instance-header-report-series-past-due-grouped-by-process-template-header-for-user-group?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/processPlan/latest/actions/list-process-instance-header-report-series-past-due-grouped-by-process-template-header-for-user-group?${params}`, {
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
| `userGroupId` | string | no | User group ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Process Plan API returns.

## Native endpoint

Through the native Process Plan API, this operation is `GET /user_group/:userGroupId/process_instance_header_report_series/list/past_due/grouped_by/process_template_header` (base URL `https://apius0.processplan.com/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-process-instance-header-report-series-past-due-grouped-by-process-template-header-for-user-group.md) for the provider-specific parameters and requirements.

