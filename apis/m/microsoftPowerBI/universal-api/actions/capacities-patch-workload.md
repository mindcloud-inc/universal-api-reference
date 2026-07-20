# Microsoft Power BI: Patch Workload



```
PUT https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/capacities-patch-workload
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Power BI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/capacities-patch-workload" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "capacityId": "string",
  "workloadName": "Ava Chen",
  "state": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/capacities-patch-workload', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "capacityId": "string",
    "workloadName": "Ava Chen",
    "state": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `capacityId` | string | yes | The capacity ID |
| `workloadName` | string | yes | The name of the workload |
| `state` | object | yes | The capacity workload state |
| `maxMemoryPercentageSetByUser` | number | no | The percentage of the maximum memory that a workload can consume (set by the user) |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Microsoft Power BI API returns.

## Native endpoint

Through the native Microsoft Power BI API, this operation is `PATCH capacities/[:capacityId]/Workloads/[:workloadName]` (base URL `https://api.powerbi.com/v1.0/myorg`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/capacities-patch-workload.md) for the provider-specific parameters and requirements.

