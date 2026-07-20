# Housecall Pro: Get Job



```
GET https://connect.mindcloud.co/v1/universal/housecallPro/latest/actions/get-job
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Housecall Pro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/housecallPro/latest/actions/get-job?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/housecallPro/latest/actions/get-job?${params}`, {
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
| `id` | string | yes | The ID of the job. |
| `expand` | list | no | Fields to expand in the response body. One of: `appointments`, `attachments`. Accepts multiple values as an array. |

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

Through the native Housecall Pro API, this operation is `GET /jobs/:id` (base URL `https://api.housecallpro.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-job.md) for the provider-specific parameters and requirements.

