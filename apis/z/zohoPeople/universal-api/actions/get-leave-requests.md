# Zoho People: Get Leave Requests

Retrieves leave requests from Zoho People.

```
GET https://connect.mindcloud.co/v1/universal/zohoPeople/latest/actions/get-leave-requests
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho People `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoPeople/latest/actions/get-leave-requests?connectionId=$CONNECTION_ID&fromDate=string&toDate=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fromDate": "string",
  "toDate": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoPeople/latest/actions/get-leave-requests?${params}`, {
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
| `fromDate` | string | yes | Start date for the leave search, in the organization date format. |
| `toDate` | string | yes | End date for the leave search, in the organization date format. |
| `dataSelect` | string | no | Choose which employee scope to fetch, such as MINE, SUBORDINATES, or ALL. Default: `ALL`. |
| `approvalStatus` | string | no | Filter by approval status. Zoho defaults this to ALL. Default: `ALL`. |
| `offset` | number | no | Start index for the leave records to fetch. Default: `1`. |
| `limit` | number | no | Optional maximum number of leave records to fetch. |
| `sort` | string | no | Sort expression such as leave_type, -leave_type, employee, or -from_date. |
| `employeeZohoIds` | string | no | Optional JSON array of employee erecnos to filter by. |
| `employeeDepartmentIds` | string | no | Optional JSON array of department IDs to filter by. |
| `employeeLocationIds` | string | no | Optional JSON array of location IDs to filter by. |
| `employeeStatus` | string | no | Optional JSON array of status values such as ACTIVE_USERS or EX_EMPLOYEES. |
| `leaveTypeIds` | string | no | Optional JSON array of leave type IDs to filter by. |
| `typeOfLeave` | string | no | Optional JSON array of leave categories such as PAID or UNPAID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "approval_status": "string",
      "date_of_request": "string",
      "days": {},
      "employee": {
        "avatar": "string",
        "id": "string",
        "name": "Ava Chen",
        "zoho_id": 1
      },
      "from_date": "string",
      "leave_id": 1,
      "leave_type": {
        "id": 1,
        "name": "Ava Chen",
        "type": "string"
      },
      "Reason": "string",
      "to_date": "string",
      "unit": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `approval_status` | string |  |
| `date_of_request` | string |  |
| `days` | object |  |
| `employee.avatar` | string |  |
| `employee.id` | string |  |
| `employee.name` | string |  |
| `employee.zoho_id` | number |  |
| `from_date` | string |  |
| `leave_id` | number |  |
| `leave_type.id` | number |  |
| `leave_type.name` | string |  |
| `leave_type.type` | string |  |
| `Reason` | string |  |
| `to_date` | string |  |
| `unit` | string |  |

## Native endpoint

Through the native Zoho People API, this operation is `GET /api/v3/leave-tracker/leaves` (base URL `https://people.zoho.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-leave-requests.md) for the provider-specific parameters and requirements.

