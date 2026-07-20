# ServiceTitan: Create Job



```
POST https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/create-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServiceTitan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/create-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerId": 1,
  "locationId": 1,
  "businessUnitId": 1,
  "jobTypeId": 1,
  "priority": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/create-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerId": 1,
    "locationId": 1,
    "businessUnitId": 1,
    "jobTypeId": 1,
    "priority": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `appointments[].start` | string | no |  |
| `customerId` | number | yes |  |
| `customFields[].typeId` | number | no |  |
| `externalData.applicationGuid` | string | no |  |
| `externalData.externalDataItems[].key` | string | no |  |
| `appointments[].end` | string | no |  |
| `customFields[].value` | string | no |  |
| `externalData.externalDataItems[]` | array | no |  |
| `externalData.externalDataItems[].value` | string | no |  |
| `locationId` | number | yes |  |
| `appointments[].arrivalWindowStart` | string | no |  |
| `projectId` | number | no |  |
| `appointments[].arrivalWindowEnd` | string | no |  |
| `businessUnitId` | number | yes |  |
| `appointments[].technicianIds` | string | no | Accepts multiple values as an array. |
| `jobTypeId` | number | yes |  |
| `priority` | string | yes |  |
| `campaignId` | number | no |  |
| `summary` | string | no |  |
| `customerPo` | string | no |  |
| `customFields[]` | array | no |  |
| `summary` | string | no |  |
| `appointments[]` | array | no |  |
| `jobStatus` | string | no |  |
| `externalData` | object | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ServiceTitan API returns.

## Native endpoint

Through the native ServiceTitan API, this operation is `POST jpm/v2/tenant/{{credentials.tenant}}/jobs` (base URL `https://{{credentials.baseUrl}}/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-job.md) for the provider-specific parameters and requirements.

