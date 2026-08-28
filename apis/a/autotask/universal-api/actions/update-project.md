# Autotask: Update Project



```
PUT https://connect.mindcloud.co/v1/universal/autotask/latest/actions/update-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Autotask `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/autotask/latest/actions/update-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/autotask/latest/actions/update-project', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes |  |
| `projectName` | string | no |  |
| `projectType` | number | no | Baseline projects are read-only and cannot be updated through the API. |
| `startDateTime` | date | no | Can be changed only when no phases, tasks, or issues are associated, and must be before the end date. Example: `2026-08-27`. |
| `endDateTime` | date | no | Must be on or after the latest phase, task, or issue end date. Example: `2026-08-28`. |
| `projectLeadResourceId` | number | no |  |
| `contractId` | number | no |  |
| `opportunityId` | number | no |  |
| `organizationalLevelAssociationId` | number | no |  |
| `department` | number | no |  |
| `status` | number | no | Inactive status inactivates the project; completing a project also completes its associated tasks. |
| `completedDateTime` | date | no | Example: `2026-08-27`. |
| `statusDateTime` | date | no | Example: `2026-08-27`. |
| `statusDetail` | string | no |  |
| `description` | string | no |  |
| `extProjectNumber` | string | no |  |
| `extProjectType` | number | no |  |
| `purchaseOrderNumber` | string | no |  |
| `estimatedSalesCost` | number | no |  |
| `laborEstimatedCosts` | number | no |  |
| `laborEstimatedRevenue` | number | no |  |
| `originalEstimatedRevenue` | number | no |  |
| `projectCostsBudget` | number | no |  |
| `projectCostsRevenue` | number | no |  |
| `sGda` | number | no |  |
| `userDefinedFields[]` | array<object> | no | Optional project user-defined fields. Multi-select and reference UDFs are not supported. |
| `userDefinedFields[].name` | string | no |  |
| `userDefinedFields[].value` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Autotask API returns.

## Native endpoint

Through the native Autotask API, this operation is `PATCH /Projects` (base URL `https://webservices14.autotask.net/ATServicesRest/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-project.md) for the provider-specific parameters and requirements.

