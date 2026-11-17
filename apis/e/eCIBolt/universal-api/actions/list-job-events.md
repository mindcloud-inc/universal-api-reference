# ECI Bolt: List Job Events



```
GET https://connect.mindcloud.co/v1/universal/eCIBolt/latest/actions/list-job-events
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ECI Bolt `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/eCIBolt/latest/actions/list-job-events?connectionId=$CONNECTION_ID&eventToken=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "eventToken": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/eCIBolt/latest/actions/list-job-events?${params}`, {
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
| `eventToken` | string | yes | Token used to get the next list of events. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "events": [
        {
          "author": "string",
          "authorId": 1,
          "changes": {},
          "createdAt": "string",
          "event": "string",
          "job": {
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
        }
      ],
      "eventToken": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `events` | array<object> |  |
| `events[].author` | string |  |
| `events[].authorId` | number |  |
| `events[].changes` | object |  |
| `events[].createdAt` | string |  |
| `events[].event` | string |  |
| `events[].job` | object |  |
| `events[].job.accountingNumber` | string |  |
| `events[].job.active` | boolean |  |
| `events[].job.address` | string |  |
| `events[].job.block` | string |  |
| `events[].job.builderJobNumber` | string |  |
| `events[].job.city` | string |  |
| `events[].job.closeDate` | date |  |
| `events[].job.community` | string |  |
| `events[].job.communityExternalId` | string |  |
| `events[].job.communityId` | number |  |
| `events[].job.createdAt` | string |  |
| `events[].job.customer` | string |  |
| `events[].job.customerExternalId` | string |  |
| `events[].job.customerId` | number |  |
| `events[].job.customField1` | string |  |
| `events[].job.customField2` | string |  |
| `events[].job.etag` | string |  |
| `events[].job.floorplan` | string |  |
| `events[].job.floorplanId` | number |  |
| `events[].job.homeOwner` | string |  |
| `events[].job.homeOwnerEmail` | string |  |
| `events[].job.homeOwnerPhone` | string |  |
| `events[].job.id` | number |  |
| `events[].job.jobType` | string |  |
| `events[].job.jobTypeId` | number |  |
| `events[].job.lot` | string |  |
| `events[].job.municipality` | string |  |
| `events[].job.notes` | string |  |
| `events[].job.office` | string |  |
| `events[].job.officeId` | number |  |
| `events[].job.permitDate` | date |  |
| `events[].job.permitNumber` | string |  |
| `events[].job.squareFootage` | number |  |
| `events[].job.startDate` | date |  |
| `events[].job.underWarranty` | boolean |  |
| `events[].job.updatedAt` | string |  |
| `events[].job.zip` | string |  |
| `eventToken` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native ECI Bolt API, this operation is `GET /open/v1/jobs/events` (base URL `https://app.bolttech.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-job-events.md) for the provider-specific parameters and requirements.

