# Leave Dates: Get Employment Report

Retrieves employment report rows from Leave Dates.

```
GET https://connect.mindcloud.co/v1/universal/leaveDates/latest/actions/get-employment-report
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Leave Dates `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leaveDates/latest/actions/get-employment-report?connectionId=$CONNECTION_ID&company=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "company": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/leaveDates/latest/actions/get-employment-report?${params}`, {
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
| `company` | string | yes | Company ID |
| `department` | string | no | Department ID |
| `reportType` | string | no | Selected type of the report |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allowanceUnit": "string",
      "dateOfBirth": "string",
      "departmentName": "Ava Chen",
      "email": "ava@example.com",
      "employeeCode": "string",
      "endDate": "string",
      "fullName": "Ava Chen",
      "holidayLocation": "string",
      "hoursPerWorkingDay": 1,
      "id": "string",
      "isAdmin": "string",
      "isApprover": "string",
      "jobTitle": "string",
      "startDate": "string",
      "timezone": "string",
      "yearsOfService": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowanceUnit` | string | Allowance unit shown for the employment. |
| `dateOfBirth` | string | Date of birth value when present. |
| `departmentName` | string | Department name shown in the report row. |
| `email` | string | Employment email address. |
| `employeeCode` | string | Employee code shown in the report row. |
| `endDate` | string | Employment end date when present. |
| `fullName` | string | Employment full name from the report row. |
| `holidayLocation` | string | Holiday location shown in the report row. |
| `hoursPerWorkingDay` | number | Hours per working day for the employment. |
| `id` | string | Employment record ID from the report row. |
| `isAdmin` | string | Whether the employment is an admin according to the report row. |
| `isApprover` | string | Whether the employment is an approver according to the report row. |
| `jobTitle` | string | Job title reported for the employment row. |
| `startDate` | string | Employment start date when present. |
| `timezone` | string | Timezone assigned to the employment. |
| `yearsOfService` | string | Years-of-service value when present. |

## Native endpoint

Through the native Leave Dates API, this operation is `GET /reports/employments` (base URL `https://api.leavedates.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-employment-report.md) for the provider-specific parameters and requirements.

