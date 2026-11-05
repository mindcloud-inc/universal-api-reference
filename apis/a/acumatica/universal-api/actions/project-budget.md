# Acumatica: Project Budget

Create or update a project budget line, including account group, cost code, type, description, original budgeted quantity, UOM, original budgeted amount, completion percentage, and pending invoice amount.

```
PUT https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/project-budget
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Acumatica `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/project-budget" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/project-budget', {
  method: 'PUT',
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
| `accountGroup.value` | string | no |  |
| `completed.value` | number | no |  |
| `costCode.value` | string | no |  |
| `description.value` | string | no |  |
| `inventoryId.value` | string | no |  |
| `originalBudgetedAmount.value` | number | no |  |
| `originalBudgetedQty.value` | number | no |  |
| `pendingInvoiceAmount.value` | number | no |  |
| `projectId` | object | no |  |
| `projectId.value` | string | no |  |
| `projectTaskId.value` | string | no |  |
| `type.value` | string | no |  |
| `uom.value` | string | no |  |
| `projectTaskId` | object | no |  |
| `inventoryId` | object | no |  |
| `completed` | object | no |  |
| `pendingInvoiceAmount` | object | no |  |
| `accountGroup` | object | no |  |
| `costCode` | object | no |  |
| `type` | object | no |  |
| `description` | object | no |  |
| `originalBudgetedQty` | object | no |  |
| `uom` | object | no |  |
| `originalBudgetedAmount` | object | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Acumatica API returns.

## Native endpoint

Through the native Acumatica API, this operation is `PUT /entity/{{credentials.endpointName}}/{{credentials.endpointVersion}}/ProjectBudget` (base URL `{{credentials.uRL}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/project-budget.md) for the provider-specific parameters and requirements.

