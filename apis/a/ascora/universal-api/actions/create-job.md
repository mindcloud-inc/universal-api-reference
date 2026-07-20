# Ascora: Create Job

Creates a new job in Ascora.

```
POST https://connect.mindcloud.co/v1/universal/ascora/latest/actions/create-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ascora `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ascora/latest/actions/create-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "siteCustomer.id": "62c6b0d5-6f5f-4055-8edd-52649acadfba"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ascora/latest/actions/create-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "siteCustomer.id": "62c6b0d5-6f5f-4055-8edd-52649acadfba"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `siteCustomer.id` | string | yes | ID of the site customer associated with the job. Example: `62c6b0d5-6f5f-4055-8edd-52649acadfba`. |
| `jobName` | string | no | Name of the new job. Example: `Stage 3 Test Job`. |
| `jobDescription` | string | no | Description for the new job. Example: `Created by Codex stage 3 runtime test`. |
| `pricingMethod` | string | no | Pricing method for the job. If omitted, Ascora uses the default pricing method. Example: `FIXED-PRICE`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `billingCustomer.id` | string | no | ID of the billing customer associated with the job. If omitted, Ascora uses the site's linked billing customer. Example: `62c6b0d5-6f5f-4055-8edd-52649acadfba`. |
| `completedDate` | date | no | Completion timestamp for the job. Example: `2026-03-24T10:00:00`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "job": {
        "addressLine1": "string",
        "billingCustomer": {
          "id": "string",
          "name": "Ava Chen"
        },
        "country": "string",
        "dateCreated": "2026-05-07T12:00:00.000Z",
        "jobDescription": "string",
        "jobId": "string",
        "jobName": "Ava Chen",
        "jobNumber": "string",
        "jobStatus": 1,
        "jobType": {
          "id": "string",
          "name": "Ava Chen"
        },
        "postcode": "string",
        "pricingMethod": "string",
        "siteCustomer": {
          "id": "string",
          "name": "Ava Chen"
        },
        "suburb": "string",
        "topLevelJobNumber": "string",
        "totalExTax": 1,
        "totalIncTax": 1,
        "workUndertaken": "string"
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `job.addressLine1` | string |  |
| `job.billingCustomer.id` | string |  |
| `job.billingCustomer.name` | string |  |
| `job.country` | string |  |
| `job.dateCreated` | date |  |
| `job.jobDescription` | string |  |
| `job.jobId` | string |  |
| `job.jobName` | string |  |
| `job.jobNumber` | string |  |
| `job.jobStatus` | number |  |
| `job.jobType.id` | string |  |
| `job.jobType.name` | string |  |
| `job.postcode` | string |  |
| `job.pricingMethod` | string |  |
| `job.siteCustomer.id` | string |  |
| `job.siteCustomer.name` | string |  |
| `job.suburb` | string |  |
| `job.topLevelJobNumber` | string |  |
| `job.totalExTax` | number |  |
| `job.totalIncTax` | number |  |
| `job.workUndertaken` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Ascora API, this operation is `POST /Jobs/Job` (base URL `https://api.ascora.com.au`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-job.md) for the provider-specific parameters and requirements.

