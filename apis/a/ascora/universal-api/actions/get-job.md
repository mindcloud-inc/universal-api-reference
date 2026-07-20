# Ascora: Get Job

Retrieves a job from Ascora.

```
GET https://connect.mindcloud.co/v1/universal/ascora/latest/actions/get-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ascora `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ascora/latest/actions/get-job?connectionId=$CONNECTION_ID&jobNumber=J1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobNumber": "J1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ascora/latest/actions/get-job?${params}`, {
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
| `jobNumber` | string | yes | Full job number to retrieve. Example: `J1`. |

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

Through the native Ascora API, this operation is `GET /Jobs/Job/{{jobNumber}}` (base URL `https://api.ascora.com.au`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-job.md) for the provider-specific parameters and requirements.

