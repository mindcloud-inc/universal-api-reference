# Microsoft Dynamics 365: Create WBS Activity Estimate



```
POST https://connect.mindcloud.co/v1/universal/microsoftDynamics365/latest/actions/create-wbs-activity-estimate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Dynamics 365 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/microsoftDynamics365/latest/actions/create-wbs-activity-estimate" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoftDynamics365/latest/actions/create-wbs-activity-estimate', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `WBSId` | string | no |  |
| `ProjectId` | string | no |  |
| `Category` | string | no |  |
| `ResourceCategory` | string | no |  |
| `ItemNumber` | string | no |  |
| `SalesCategory` | string | no |  |
| `LineProperty` | string | no |  |
| `Quantity` | number | no |  |
| `UnitCostPrice` | number | no |  |
| `UnitSalesPrice` | number | no |  |
| `Description` | string | no |  |
| `TotalSalesPrice` | number | no |  |
| `TotalCostPrice` | number | no |  |
| `TaskName` | string | no |  |
| `TCIRoomQty` | number | no |  |
| `dataAreaId` | string | no |  |
| `TransactionType` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Microsoft Dynamics 365 API returns.

## Native endpoint

Through the native Microsoft Dynamics 365 API, this operation is `POST ProjWBSActivityEstimates` (base URL `{{credentials.baseURL}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-wbs-activity-estimate.md) for the provider-specific parameters and requirements.

