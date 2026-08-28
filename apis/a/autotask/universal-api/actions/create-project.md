# Autotask: Create Project



```
POST https://connect.mindcloud.co/v1/universal/autotask/latest/actions/create-project
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Autotask `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/autotask/latest/actions/create-project" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "companyId": 1,
  "projectName": "Ava Chen",
  "projectType": 1,
  "startDateTime": "2026-08-18",
  "endDateTime": "2026-08-19"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/autotask/latest/actions/create-project', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "companyId": 1,
    "projectName": "Ava Chen",
    "projectType": 1,
    "startDateTime": "2026-08-18",
    "endDateTime": "2026-08-19"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `companyId` | number | yes | Required when creating a project; Autotask does not allow changing the company after creation. |
| `projectName` | string | yes |  |
| `projectType` | number | yes | Baseline projects cannot be created, updated, or deleted through the API. |
| `startDateTime` | date | yes | Must be before the end date. Autotask ignores any time component. Example: `2026-08-18`. |
| `endDateTime` | date | yes | Must be on or after the end date of the latest phase, task, or issue. Autotask ignores any time component. Example: `2026-08-19`. |
| `projectLeadResourceId` | number | no |  |
| `contractId` | number | no |  |
| `opportunityId` | number | no |  |
| `organizationalLevelAssociationId` | number | no |  |
| `department` | number | no |  |
| `status` | number | no | Inactive status inactivates the project; completing a project also completes its associated tasks. |
| `completedDateTime` | date | no | Example: `2026-08-19`. |
| `statusDateTime` | date | no | Example: `2026-08-19`. |
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
| `userDefinedFields[].name` | string | no | Example: `CustomerRanking`. |
| `userDefinedFields[].value` | string | no | Example: `not Golden`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Autotask API returns.

## Native endpoint

Through the native Autotask API, this operation is `POST /Projects` (base URL `https://webservices14.autotask.net/ATServicesRest/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-project.md) for the provider-specific parameters and requirements.

