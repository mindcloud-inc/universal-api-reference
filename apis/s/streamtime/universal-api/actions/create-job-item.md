# Streamtime: Create Job Item



```
POST https://connect.mindcloud.co/v1/universal/streamtime/latest/actions/create-job-item
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Streamtime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/streamtime/latest/actions/create-job-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "jobId": "601",
  "jobPhaseId": "3",
  "jobItemStatus.id": "1",
  "name": "UI Design",
  "costingMethod.id": "1",
  "isBillable": "true",
  "timeAllocationMethod.id": "1"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/streamtime/latest/actions/create-job-item', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "jobId": "601",
    "jobPhaseId": "3",
    "jobItemStatus.id": "1",
    "name": "UI Design",
    "costingMethod.id": "1",
    "isBillable": "true",
    "timeAllocationMethod.id": "1"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `jobId` | number | yes | Job ID Example: `601`. |
| `jobPhaseId` | number | yes | Job phase ID Example: `3`. |
| `jobItemStatus` | object | no | Status of a Job item. |
| `jobItemStatus.id` | number | yes | Job Item Status ID (1=Planning, 4=Scheduled, 2=Complete, 3=Deleted) Example: `1`. |
| `name` | string | yes | Job item name Example: `UI Design`. |
| `description` | string | no | Job item description Example: `Wireframes and high-fidelity mockups`. |
| `sellRate` | number | no | Explicit sell rate in job currency (if provided) Example: `120`. |
| `costingMethod` | object | no | Consting Method |
| `costingMethod.id` | number | yes | Consting Method ID (1=Item, 2=People, 3=Fixed Price Calculated Sell, 4=Fixed Price User Sell) Example: `1`. |
| `isBillable` | boolean | yes | Is this job item billable Example: `true`. |
| `timeAllocationMethod` | object | no | How the time of an item is allocated, whether as a bucket that is shared amongst all users or individually assigned to each user. |
| `timeAllocationMethod.id` | number | yes | Time Allocation Method ID (1=Item, 2=People) Example: `1`. |
| `totalPlannedMinutes` | number | no | Total planned minutes for the item Example: `240`. |
| `estimatedStartDate` | date | no | Estimated start date Example: `2025-02-01`. |
| `estimatedEndDate` | date | no | Estimated end date Example: `2025-03-15`. |
| `completedDate` | date | no | Completion date Example: `2025-03-18`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "costingMethod": {},
      "description": "string",
      "id": 1,
      "isBillable": true,
      "jobId": 1,
      "jobItemStatus": {},
      "jobPhaseId": 1,
      "name": "Ava Chen",
      "orderId": 1,
      "timeAllocationMethod": {},
      "totalLoggedMinutes": 1,
      "totalPlannedMinutes": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `costingMethod` | object | Costing method |
| `description` | string | Job item description |
| `id` | number | Job item ID |
| `isBillable` | boolean | Whether the item is billable |
| `jobId` | number | Parent job ID |
| `jobItemStatus` | object | Current job item status |
| `jobPhaseId` | number | Parent phase ID |
| `name` | string | Job item name |
| `orderId` | number | Item order |
| `timeAllocationMethod` | object | Time allocation method |
| `totalLoggedMinutes` | number | Logged minutes |
| `totalPlannedMinutes` | number | Planned minutes |

## Native endpoint

Through the native Streamtime API, this operation is `POST /jobs/:job_id/job_items` (base URL `https://api.streamtime.net/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-job-item.md) for the provider-specific parameters and requirements.

