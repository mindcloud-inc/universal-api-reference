# Housecall Pro: List Jobs



```
GET https://connect.mindcloud.co/v1/universal/housecallPro/latest/actions/list-jobs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Housecall Pro `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/housecallPro/latest/actions/list-jobs?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/housecallPro/latest/actions/list-jobs?${params}`, {
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
| `customerId` | string | no | Filters jobs by a single customer ID. |
| `workStatus` | list | no | Returns jobs from selected work statuses. One of: `canceled`, `completed`, `in_progress`, `scheduled`, `unscheduled`. Accepts multiple values as an array. |
| `expand` | list | no | Fields to expand in the response body. One of: `appointments`, `attachments`. Accepts multiple values as an array. |
| `scheduledStartMin` | date | no | Filters jobs with a starting time greater than or equal to this date. |
| `scheduledStartMax` | date | no | Filters jobs with a starting time less than or equal to this date. |
| `scheduledEndMin` | date | no | Filters jobs with an end time greater than or equal to this date. |
| `scheduledEndMax` | date | no | Filters jobs with an end time less than or equal to this date. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `employeeIds[]` | array<string> | no |  |
| `locationIds[]` | array<string> | no | IDs of locations to pull from. Ignored when X-Company-Id is set. |

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

Through the native Housecall Pro API, this operation is `GET /jobs` (base URL `https://api.housecallpro.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-jobs.md) for the provider-specific parameters and requirements.

