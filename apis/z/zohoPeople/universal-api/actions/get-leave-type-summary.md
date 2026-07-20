# Zoho People: Get Leave Type Summary

Retrieves leave type summary from Zoho People.

```
GET https://connect.mindcloud.co/v1/universal/zohoPeople/latest/actions/get-leave-type-summary
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho People `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoPeople/latest/actions/get-leave-type-summary?connectionId=$CONNECTION_ID&leaveTypeId=string&fromDate=string&toDate=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "leaveTypeId": "string",
  "fromDate": "string",
  "toDate": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoPeople/latest/actions/get-leave-type-summary?${params}`, {
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
| `leaveTypeId` | string | yes | Leave type ID for the summary report. |
| `fromDate` | string | yes | Start date for the report, in the organization date format. |
| `toDate` | string | yes | End date for the report, in the organization date format. |
| `offset` | number | no | Start index for the report rows to fetch. Default: `1`. |
| `limit` | number | no | Optional maximum number of rows to fetch. |
| `employeeZohoIds` | string | no | Optional JSON array of employee erecnos to include. |
| `employeeDepartmentIds` | string | no | Optional JSON array of department IDs to include. |
| `employeeDesignationIds` | string | no | Optional JSON array of designation IDs to include. |
| `employeeLocationIds` | string | no | Optional JSON array of location IDs to include. |
| `employeeRoleIds` | string | no | Optional JSON array of role IDs to include. |
| `employeeStatus` | string | no | Optional JSON array of employee status values such as ACTIVE_USERS or EX_EMPLOYEES. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "booked": 1,
      "closing_balance": 1,
      "employee": {
        "id": "string",
        "name": "Ava Chen",
        "zoho_id": 1
      },
      "encashed": 1,
      "granted": 1,
      "lapsed": 1,
      "lop": 1,
      "opening_balance": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `booked` | number |  |
| `closing_balance` | number |  |
| `employee.id` | string |  |
| `employee.name` | string |  |
| `employee.zoho_id` | number |  |
| `encashed` | number |  |
| `granted` | number |  |
| `lapsed` | number |  |
| `lop` | number |  |
| `opening_balance` | number |  |

## Native endpoint

Through the native Zoho People API, this operation is `GET /api/v3/leave-tracker/reports/leave-type-summary/:leaveTypeId` (base URL `https://people.zoho.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-leave-type-summary.md) for the provider-specific parameters and requirements.

