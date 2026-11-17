# ECI Bolt: Create Job



```
POST https://connect.mindcloud.co/v1/universal/eCIBolt/latest/actions/create-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ECI Bolt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/eCIBolt/latest/actions/create-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "job.address": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/eCIBolt/latest/actions/create-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "job.address": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `job.address` | string | yes |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `job` | object | no |  |
| `job.lot` | string | no |  |
| `job.block` | string | no |  |
| `job.active` | boolean | no |  |
| `job.permitNumber` | string | no |  |
| `job.permitDate` | date | no | Bolt expects this date as MM/DD/YYYY. |
| `job.startDate` | date | no | Bolt expects this date as MM/DD/YYYY. |
| `job.builderJobNumber` | string | no |  |
| `job.notes` | string | no |  |
| `job.zip` | string | no |  |
| `job.accountingNumber` | string | no |  |
| `job.underWarranty` | boolean | no |  |
| `job.municipality` | string | no |  |
| `job.skipAddressUniqueness` | boolean | no |  |
| `job.floorplanId` | number | no |  |
| `job.jobTypeId` | number | no |  |
| `job.createContractualWorkOrders` | boolean | no |  |
| `job.notKnown` | boolean | no |  |
| `job.builderService` | boolean | no |  |
| `job.communityId` | number | no |  |
| `job.cityId` | number | no |  |
| `job.customerId` | number | no |  |
| `job.supervisorId` | number | no |  |
| `job.closeDate` | date | no | Bolt expects this date as MM/DD/YYYY. |
| `job.squareFootage` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountingNumber": "string",
      "active": true,
      "address": "string",
      "block": "string",
      "builderJobNumber": "string",
      "city": "string",
      "closeDate": "2026-05-07T12:00:00.000Z",
      "community": "string",
      "communityExternalId": "string",
      "communityId": 1,
      "createdAt": "string",
      "customer": "string",
      "customerExternalId": "string",
      "customerId": 1,
      "customField1": "string",
      "customField2": "string",
      "etag": "string",
      "floorplan": "string",
      "floorplanId": 1,
      "homeOwner": "string",
      "homeOwnerEmail": "ava@example.com",
      "homeOwnerPhone": "string",
      "id": 1,
      "jobType": "string",
      "jobTypeId": 1,
      "lot": "string",
      "municipality": "string",
      "notes": "string",
      "office": "string",
      "officeId": 1,
      "permitDate": "2026-05-07T12:00:00.000Z",
      "permitNumber": "string",
      "squareFootage": 1,
      "startDate": "2026-05-07T12:00:00.000Z",
      "underWarranty": true,
      "updatedAt": "string",
      "zip": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountingNumber` | string |  |
| `active` | boolean |  |
| `address` | string |  |
| `block` | string |  |
| `builderJobNumber` | string |  |
| `city` | string |  |
| `closeDate` | date |  |
| `community` | string |  |
| `communityExternalId` | string |  |
| `communityId` | number |  |
| `createdAt` | string |  |
| `customer` | string |  |
| `customerExternalId` | string |  |
| `customerId` | number |  |
| `customField1` | string |  |
| `customField2` | string |  |
| `etag` | string |  |
| `floorplan` | string |  |
| `floorplanId` | number |  |
| `homeOwner` | string |  |
| `homeOwnerEmail` | string |  |
| `homeOwnerPhone` | string |  |
| `id` | number |  |
| `jobType` | string |  |
| `jobTypeId` | number |  |
| `lot` | string |  |
| `municipality` | string |  |
| `notes` | string |  |
| `office` | string |  |
| `officeId` | number |  |
| `permitDate` | date |  |
| `permitNumber` | string |  |
| `squareFootage` | number |  |
| `startDate` | date |  |
| `underWarranty` | boolean |  |
| `updatedAt` | string |  |
| `zip` | string |  |

## Native endpoint

Through the native ECI Bolt API, this operation is `POST /open/v1/jobs` (base URL `https://app.bolttech.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-job.md) for the provider-specific parameters and requirements.

