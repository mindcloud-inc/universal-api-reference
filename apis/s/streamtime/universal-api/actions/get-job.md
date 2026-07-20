# Streamtime: Get Job



```
GET https://connect.mindcloud.co/v1/universal/streamtime/latest/actions/get-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Streamtime `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/streamtime/latest/actions/get-job?connectionId=$CONNECTION_ID&jobId=601" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "601"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/streamtime/latest/actions/get-job?${params}`, {
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
      "branchId": 1,
      "companyId": 1,
      "createdUserId": 1,
      "estimatedEndDate": "string",
      "estimatedStartDate": "string",
      "finalBudget": 1,
      "fullName": "Ava Chen",
      "id": 1,
      "isBillable": true,
      "jobCreatedDatetime": "string",
      "jobCurrencyFinalBudget": 1,
      "jobStatus": {},
      "name": "Ava Chen",
      "number": "string",
      "rateCardId": 1,
      "totalApprovedQuoteExTax": 1,
      "totalDraftInvoicesExTax": 1,
      "totalIncompleteMinutes": 1,
      "totalInvoicedExTax": 1,
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
| `branchId` | number | Branch ID |
| `companyId` | number | Company ID |
| `createdUserId` | number | Created by user ID |
| `estimatedEndDate` | string | Estimated end date |
| `estimatedStartDate` | string | Estimated start date |
| `finalBudget` | number | Final budget amount |
| `fullName` | string | Job display name |
| `id` | number | Job ID |
| `isBillable` | boolean | Whether the job is billable |
| `jobCreatedDatetime` | string | Job created timestamp |
| `jobCurrencyFinalBudget` | number | Final budget in job currency |
| `jobStatus` | object | Current job status |
| `name` | string | Job name |
| `number` | string | Job number |
| `rateCardId` | number | Rate card ID |
| `totalApprovedQuoteExTax` | number | Total approved quote excluding tax |
| `totalDraftInvoicesExTax` | number | Total draft invoices excluding tax |
| `totalIncompleteMinutes` | number | Total incomplete minutes |
| `totalInvoicedExTax` | number | Total invoiced excluding tax |
| `totalLoggedMinutes` | number | Total logged minutes |
| `totalPlannedMinutes` | number | Total planned minutes |

## Native endpoint

Through the native Streamtime API, this operation is `GET /jobs/:job_id` (base URL `https://api.streamtime.net/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-job.md) for the provider-specific parameters and requirements.

