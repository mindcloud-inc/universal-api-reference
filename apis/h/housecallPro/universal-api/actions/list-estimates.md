# Housecall Pro: List Estimates



```
GET https://connect.mindcloud.co/v1/universal/housecallPro/latest/actions/list-estimates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Housecall Pro `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/housecallPro/latest/actions/list-estimates?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/housecallPro/latest/actions/list-estimates?${params}`, {
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
| `customerId` | string | no | Filters estimates by a single customer ID. Example: `cus_123`. |
| `workStatus` | list<string> | no | Work status filter. Returns estimates from all statuses if empty. One of: `canceled`, `completed`, `in_progress`, `scheduled`, `unscheduled`. Accepts multiple values as an array. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `scheduledStartMin` | date | no | Filters estimates with a starting time greater than or equal to the date sent. Example: `2024-01-30T00:00:00Z`. |
| `scheduledStartMax` | date | no | Filters estimates with a starting time less than or equal to the date sent. Example: `2024-01-30T00:00:00Z`. |
| `scheduledEndMin` | date | no | Filters estimates with an end time greater than or equal to the date sent. Example: `2024-01-30T00:00:00Z`. |
| `scheduledEndMax` | date | no | Filters estimates with an end time less than or equal to the date sent. Example: `2024-01-30T00:00:00Z`. |
| `employeeIds[]` | array<string> | no | Filters estimates by assigned pro id. Accepts multiple values as an array. |
| `locationIds[]` | array<string> | no | IDs of locations you want to pull from. Accepts multiple values as an array. |
| `expand` | list<string> | no | Array of strings to expand response body. One of: `attachments`. Accepts multiple values as an array. |

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
      "companyId": "string",
      "companyName": "Ava Chen",
      "createdAt": "string",
      "customer": {},
      "estimateFields": {},
      "estimateNumber": "string",
      "id": "string",
      "leadSource": "string",
      "options": [
        {}
      ],
      "schedule": {},
      "updatedAt": "string",
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
| `address` | object |  |
| `assignedEmployees` | array<object> |  |
| `companyId` | string |  |
| `companyName` | string |  |
| `createdAt` | string |  |
| `customer` | object |  |
| `estimateFields` | object |  |
| `estimateNumber` | string |  |
| `id` | string |  |
| `leadSource` | string |  |
| `options` | array<object> |  |
| `schedule` | object |  |
| `updatedAt` | string |  |
| `workStatus` | string |  |
| `workTimestamps` | object |  |

## Native endpoint

Through the native Housecall Pro API, this operation is `GET /estimates` (base URL `https://api.housecallpro.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-estimates.md) for the provider-specific parameters and requirements.

