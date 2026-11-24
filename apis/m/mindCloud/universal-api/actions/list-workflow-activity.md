# MindCloud: List Workflow Activity



```
GET https://connect.mindcloud.co/v1/universal/mindCloud/latest/actions/list-workflow-activity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MindCloud `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mindCloud/latest/actions/list-workflow-activity?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mindCloud/latest/actions/list-workflow-activity?${params}`, {
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
| `workflowId` | list<string> | no | Only rows of this workflow. Example: `Wq3kZ8pLx2Nb`. |
| `from` | string | no | First day of the window, as YYYY-MM-DD (UTC). Defaults to 29 days before To. Example: `2026-11-01`. |
| `to` | string | no | Last day of the window, as YYYY-MM-DD (UTC), included. Defaults to today. A window covers at most 92 days. Example: `2026-11-23`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "date": "2026-05-07T12:00:00.000Z",
      "failedRuns": 1,
      "id": "string",
      "recordsCreated": 1,
      "recordsDeleted": 1,
      "recordsRead": 1,
      "recordsUpdated": 1,
      "runs": 1,
      "workflowId": "string",
      "workflowName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date` | date | The UTC day the runs started. |
| `failedRuns` | number | How many of those runs failed. |
| `id` | string | A stable key for this row: one workflow on one day. |
| `recordsCreated` | number | Records those runs logged as created. |
| `recordsDeleted` | number | Records those runs logged as deleted. |
| `recordsRead` | number | Records those runs logged as read. |
| `recordsUpdated` | number | Records those runs logged as updated. |
| `runs` | number | Runs of the workflow that started that day. |
| `workflowId` | string | The workflow. |
| `workflowName` | string | The workflow's current name. |

## Native endpoint

Through the native MindCloud API, this operation is `GET /v2/workflow-activity` (base URL `https://connect.mindcloud.co`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-workflow-activity.md) for the provider-specific parameters and requirements.

