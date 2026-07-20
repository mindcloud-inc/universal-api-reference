# Streamtime: Create Job



```
POST https://connect.mindcloud.co/v1/universal/streamtime/latest/actions/create-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Streamtime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/streamtime/latest/actions/create-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "companyId": 1,
  "rateCardId": 1,
  "branchId": 1,
  "jobStatus.id": "1",
  "number": "JOB-2025-010",
  "name": "Website Redesign",
  "contactId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/streamtime/latest/actions/create-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "companyId": 1,
    "rateCardId": 1,
    "branchId": 1,
    "jobStatus.id": "1",
    "number": "JOB-2025-010",
    "name": "Website Redesign",
    "contactId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `companyId` | number | yes | Company ID linked to the job. |
| `jobLeadUserId` | number | no | Job lead user ID Example: `42`. |
| `rateCardId` | number | yes | The id of the rate card used for this job |
| `branchId` | number | yes | The id of the branch this job belongs to |
| `jobStatus` | object | no | Status of a Job. |
| `jobStatus.id` | number | yes | Job Status ID (5=Paused, 1=In Play, 2=Done, 3=Deleted, 4=Archived) Example: `1`. |
| `number` | string | yes | Job number Example: `JOB-2025-010`. |
| `name` | string | yes | Job name Example: `Website Redesign`. |
| `purchaseOrderNumber` | string | no | Client purchase order number Example: `PO-12345`. |
| `contactId` | number | yes | The id of the contact this job is being done for |

## Response

```json
{
  "success": true,
  "data": [
    {
      "branchId": 1,
      "companyId": 1,
      "contactId": 1,
      "fullName": "Ava Chen",
      "id": 1,
      "jobCreatedDatetime": "string",
      "jobStatus": {},
      "name": "Ava Chen",
      "number": "string",
      "rateCardId": 1,
      "totalInvoicedExTax": 1,
      "totalLoggedMinutes": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `branchId` | number | Branch ID |
| `companyId` | number | Company ID |
| `contactId` | number | Primary contact ID |
| `fullName` | string | Full job name |
| `id` | number | Job ID |
| `jobCreatedDatetime` | string | Creation timestamp |
| `jobStatus` | object | Current job status |
| `name` | string | Job name |
| `number` | string | Job number |
| `rateCardId` | number | Rate card ID |
| `totalInvoicedExTax` | number | Total invoiced excluding tax |
| `totalLoggedMinutes` | number | Total logged minutes |

## Native endpoint

Through the native Streamtime API, this operation is `POST /jobs` (base URL `https://api.streamtime.net/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-job.md) for the provider-specific parameters and requirements.

