# Ascora: List Jobs

Retrieves jobs from Ascora.

```
GET https://connect.mindcloud.co/v1/universal/ascora/latest/actions/list-jobs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ascora `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ascora/latest/actions/list-jobs?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ascora/latest/actions/list-jobs?${params}`, {
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
| `assignedUser` | string | no | Find all Jobs based on the full name of the Assigned User. |
| `customerName` | string | no | Find all Jobs with a partially matching Site or Billing Customer Name. |
| `endDate` | date | no | Search for Jobs created on or before the specified date. |
| `filterText` | string | no | Performs a partial search against the full Quote Number, Name or Address. |
| `jobStatus` | string | no | Filters the Jobs to the specified status. |
| `jobType` | string | no | Matches against the related Job Type. |
| `startDate` | date | no | Search for Jobs created on or after the specified date. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "results": [
        {
          "addressLine1": "string",
          "addressLine2": "string",
          "billingCustomer": {
            "id": "string",
            "name": "Ava Chen"
          },
          "clientOrderNumber": "string",
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
          "purchaseOrderNumber": "string",
          "siteCustomer": {
            "id": "string",
            "name": "Ava Chen"
          },
          "suburb": "string",
          "topLevelJobNumber": "string",
          "totalExTax": 1,
          "totalIncTax": 1,
          "workUndertaken": "string"
        }
      ],
      "success": true,
      "totalPages": 1,
      "totalRecords": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `results[].addressLine1` | string |  |
| `results[].addressLine2` | string |  |
| `results[].billingCustomer.id` | string |  |
| `results[].billingCustomer.name` | string |  |
| `results[].clientOrderNumber` | string |  |
| `results[].country` | string |  |
| `results[].dateCreated` | date |  |
| `results[].jobDescription` | string |  |
| `results[].jobId` | string |  |
| `results[].jobName` | string |  |
| `results[].jobNumber` | string |  |
| `results[].jobStatus` | number |  |
| `results[].jobType.id` | string |  |
| `results[].jobType.name` | string |  |
| `results[].postcode` | string |  |
| `results[].pricingMethod` | string |  |
| `results[].purchaseOrderNumber` | string |  |
| `results[].siteCustomer.id` | string |  |
| `results[].siteCustomer.name` | string |  |
| `results[].suburb` | string |  |
| `results[].topLevelJobNumber` | string |  |
| `results[].totalExTax` | number |  |
| `results[].totalIncTax` | number |  |
| `results[].workUndertaken` | string |  |
| `success` | boolean |  |
| `totalPages` | number |  |
| `totalRecords` | number |  |

## Native endpoint

Through the native Ascora API, this operation is `GET /Jobs/Jobs` (base URL `https://api.ascora.com.au`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-jobs.md) for the provider-specific parameters and requirements.

