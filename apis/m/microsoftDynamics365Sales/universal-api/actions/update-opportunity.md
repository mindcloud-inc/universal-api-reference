# Microsoft Dynamics 365 Sales: Update Opportunity



```
PUT https://connect.mindcloud.co/v1/universal/microsoftDynamics365Sales/latest/actions/update-opportunity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Dynamics 365 Sales `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/microsoftDynamics365Sales/latest/actions/update-opportunity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "opportunityId": "00000000-0000-0000-0000-000000000001"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoftDynamics365Sales/latest/actions/update-opportunity', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "opportunityId": "00000000-0000-0000-0000-000000000001"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `opportunityId` | string | yes | Example: `00000000-0000-0000-0000-000000000001`. |
| `fields` | object | no | Map an object containing only the columns to change, or fill the individual fields below. Use native column logical names for custom fields. |
| `fields.name` | string | no |  |
| `fields.description` | string | no |  |
| `fields.estimatedValue` | number | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fields.estimatedCloseDate` | date | no |  |
| `fields.closeProbability` | number | no |  |
| `fields.budgetAmount` | number | no |  |
| `fields.stepName` | string | no |  |
| `fields.isRevenueSystemCalculated` | boolean | no |  |
| `fields.currentSituation` | string | no |  |
| `fields.customerNeed` | string | no |  |
| `fields.customerPainPoints` | string | no |  |
| `fields.proposedSolution` | string | no |  |
| `select` | string | no | Comma-separated column logical names to return. Accepts multiple values in one string, delimited by `,`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Microsoft Dynamics 365 Sales API returns.

## Native endpoint

Through the native Microsoft Dynamics 365 Sales API, this operation is `PATCH /opportunities(:opportunityId)` (base URL `{{credentials.environmentUrl}}/api/data/v9.2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-opportunity.md) for the provider-specific parameters and requirements.

