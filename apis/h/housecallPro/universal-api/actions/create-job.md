# Housecall Pro: Create Job



```
POST https://connect.mindcloud.co/v1/universal/housecallPro/latest/actions/create-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Housecall Pro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/housecallPro/latest/actions/create-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "customerId": "string",
  "addressId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/housecallPro/latest/actions/create-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "customerId": "string",
    "addressId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerId` | string | yes |  |
| `addressId` | string | yes |  |
| `notes` | string | no |  |
| `leadSource` | string | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `invoiceNumber` | number | no | Invoice number must be unique across all company jobs. If blank, one is generated automatically. |
| `schedule` | object | no | Scheduling details for the job. |
| `assignedEmployeeIds[]` | array<string> | no |  |
| `lineItems[]` | array<object> | no |  |
| `tags[]` | array<string> | no |  |
| `jobFields` | object | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": {},
      "assignedEmployees": [
        {}
      ],
      "canceledAt": "2026-05-07T12:00:00.000Z",
      "companyId": "string",
      "companyName": "Ava Chen",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "customer": {},
      "deletedAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": "string",
      "invoiceNumber": "string",
      "jobFields": {},
      "leadSource": "string",
      "lockedAt": "2026-05-07T12:00:00.000Z",
      "notes": [
        {}
      ],
      "originalEstimateId": "string",
      "originalEstimateUuids": [
        "string"
      ],
      "outstandingBalance": 1,
      "recurrenceNumber": 1,
      "recurrenceRule": "string",
      "schedule": {},
      "subtotal": 1,
      "tags": [
        "string"
      ],
      "totalAmount": 1,
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "workStatus": "string",
      "workTimestamps": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | object | Job address details. |
| `assignedEmployees` | array<object> | Assigned employees. |
| `canceledAt` | date | Job cancellation timestamp. |
| `companyId` | string | Company ID. |
| `companyName` | string | Company name. |
| `createdAt` | date | Job creation timestamp. |
| `customer` | object | Customer attached to the job. |
| `deletedAt` | date | Job deletion timestamp. |
| `description` | string | Job description. |
| `id` | string | Job ID. |
| `invoiceNumber` | string | Invoice number. |
| `jobFields` | object | Job field values. |
| `leadSource` | string | Lead source. |
| `lockedAt` | date | Timestamp when the job was locked. |
| `notes` | array<object> | Job notes. |
| `originalEstimateId` | string | Original estimate ID. |
| `originalEstimateUuids` | array<string> | Original estimate UUIDs. |
| `outstandingBalance` | number | Outstanding balance. |
| `recurrenceNumber` | number | Recurrence instance number. |
| `recurrenceRule` | string | Recurrence rule. |
| `schedule` | object | Job schedule. |
| `subtotal` | number | Job subtotal. |
| `tags` | array<string> | Job tags. |
| `totalAmount` | number | Total job amount. |
| `updatedAt` | date | Job update timestamp. |
| `workStatus` | string | Work status. |
| `workTimestamps` | object | Job work timestamps. |

## Native endpoint

Through the native Housecall Pro API, this operation is `POST /jobs` (base URL `https://api.housecallpro.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-job.md) for the provider-specific parameters and requirements.

