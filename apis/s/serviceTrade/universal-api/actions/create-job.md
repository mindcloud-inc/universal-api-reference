# ServiceTrade: Create Job

Creates a new job in ServiceTrade.

```
POST https://connect.mindcloud.co/v1/universal/serviceTrade/latest/actions/create-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServiceTrade `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/serviceTrade/latest/actions/create-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "locationId": 1,
  "vendorId": 1,
  "type": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/serviceTrade/latest/actions/create-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "locationId": 1,
    "vendorId": 1,
    "type": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `locationId` | number | yes | Location where the job is performed. |
| `vendorId` | number | yes | Vendor company performing the work. |
| `type` | string | yes | Job type to create. |
| `customName` | string | no | Optional user-facing job name. |
| `description` | string | no | Optional job description. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "assignedOffice": {
        "id": 1,
        "name": "Ava Chen",
        "refNumber": "string"
      },
      "budgeted": true,
      "contract": {
        "id": 1,
        "name": "Ava Chen"
      },
      "created": 1,
      "customer": {
        "id": 1,
        "name": "Ava Chen",
        "status": "string"
      },
      "customName": "Ava Chen",
      "displayStatus": "string",
      "dueAfter": 1,
      "dueBy": 1,
      "id": 1,
      "isProject": true,
      "location": {
        "address": {
          "city": "string",
          "state": "string"
        },
        "id": 1,
        "name": "Ava Chen",
        "refNumber": "string",
        "status": "string"
      },
      "name": "Ava Chen",
      "number": 1,
      "owner": {
        "email": "ava@example.com",
        "id": 1,
        "name": "Ava Chen",
        "status": "string"
      },
      "refNumber": "string",
      "scheduledDate": 1,
      "status": "string",
      "substatus": "string",
      "type": "string",
      "updated": 1,
      "uri": "string",
      "vendor": {
        "id": 1,
        "name": "Ava Chen",
        "status": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assignedOffice.id` | number |  |
| `assignedOffice.name` | string |  |
| `assignedOffice.refNumber` | string |  |
| `budgeted` | boolean |  |
| `contract.id` | number |  |
| `contract.name` | string |  |
| `created` | number |  |
| `customer.id` | number |  |
| `customer.name` | string |  |
| `customer.status` | string |  |
| `customName` | string |  |
| `displayStatus` | string |  |
| `dueAfter` | number |  |
| `dueBy` | number |  |
| `id` | number |  |
| `isProject` | boolean |  |
| `location.address.city` | string |  |
| `location.address.state` | string |  |
| `location.id` | number |  |
| `location.name` | string |  |
| `location.refNumber` | string |  |
| `location.status` | string |  |
| `name` | string |  |
| `number` | number |  |
| `owner.email` | string |  |
| `owner.id` | number |  |
| `owner.name` | string |  |
| `owner.status` | string |  |
| `refNumber` | string |  |
| `scheduledDate` | number |  |
| `status` | string |  |
| `substatus` | string |  |
| `type` | string |  |
| `updated` | number |  |
| `uri` | string |  |
| `vendor.id` | number |  |
| `vendor.name` | string |  |
| `vendor.status` | string |  |

## Native endpoint

Through the native ServiceTrade API, this operation is `POST job` (base URL `https://api.servicetrade.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-job.md) for the provider-specific parameters and requirements.

