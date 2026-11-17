# ECI Bolt: List Jobs



```
GET https://connect.mindcloud.co/v1/universal/eCIBolt/latest/actions/list-jobs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ECI Bolt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eCIBolt/latest/actions/list-jobs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eCIBolt/latest/actions/list-jobs?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `refreshToken` | string | no | Token used to get the changed jobs, returned on the last page of the jobs. You should only send the refresh_token or the next_batch. |
| `refresh` | string | no | Return only directly changed records when value is "self" |

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

Through the native ECI Bolt API, this operation is `GET /open/v1/jobs` (base URL `https://app.bolttech.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-jobs.md) for the provider-specific parameters and requirements.

