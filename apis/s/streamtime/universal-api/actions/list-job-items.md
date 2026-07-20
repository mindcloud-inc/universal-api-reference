# Streamtime: List Job Items



```
GET https://connect.mindcloud.co/v1/universal/streamtime/latest/actions/list-job-items
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Streamtime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/streamtime/latest/actions/list-job-items?connectionId=$CONNECTION_ID&jobId=601" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "601"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/streamtime/latest/actions/list-job-items?${params}`, {
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
| `jobId` | number | yes | Job ID Example: `601`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "completedDate": "string",
      "costingMethod": {},
      "description": "string",
      "estimatedEndDate": "string",
      "estimatedStartDate": "string",
      "id": 1,
      "isBillable": true,
      "jobId": 1,
      "jobItemStatus": {},
      "jobPhaseId": 1,
      "name": "Ava Chen",
      "orderId": 1,
      "sellRate": 1,
      "timeAllocationMethod": {},
      "totalIncompleteMinutes": 1,
      "totalLoggedMinutes": 1,
      "totalPlannedMinutes": 1,
      "totalScheduledUsers": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `completedDate` | string | Completed date |
| `costingMethod` | object | Costing method |
| `description` | string | Job item description |
| `estimatedEndDate` | string | Estimated end date |
| `estimatedStartDate` | string | Estimated start date |
| `id` | number | Job item ID |
| `isBillable` | boolean | Whether the item is billable |
| `jobId` | number | Job ID |
| `jobItemStatus` | object | Current job item status |
| `jobPhaseId` | number | Job phase ID |
| `name` | string | Job item name |
| `orderId` | number | Job item order |
| `sellRate` | number | Sell rate |
| `timeAllocationMethod` | object | Time allocation method |
| `totalIncompleteMinutes` | number | Total incomplete minutes |
| `totalLoggedMinutes` | number | Total logged minutes |
| `totalPlannedMinutes` | number | Total planned minutes |
| `totalScheduledUsers` | number | Scheduled users count |

## Native endpoint

Through the native Streamtime API, this operation is `GET /jobs/:job_id/job_items` (base URL `https://api.streamtime.net/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-job-items.md) for the provider-specific parameters and requirements.

