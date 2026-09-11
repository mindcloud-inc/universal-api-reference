# ServiceTitan: Get Technician Payroll Settings

Retrieves payroll settings from ServiceTitan for a technician.

```
GET https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/get-technician-payroll-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServiceTitan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/get-technician-payroll-settings?connectionId=$CONNECTION_ID&technician=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "technician": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/get-technician-payroll-settings?${params}`, {
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
| `technician` | number | yes | The technician identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "createdOn": "2026-05-07T12:00:00.000Z",
      "customFields": [
        {}
      ],
      "employeeId": 1,
      "employeeType": "string",
      "externalPayrollId": "string",
      "hireDate": "2026-05-07T12:00:00.000Z",
      "hourlyRate": 1,
      "isIncludedInPayroll": true,
      "managerId": 1,
      "modifiedOn": "2026-05-07T12:00:00.000Z",
      "payrollBusinessUnitId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `createdOn` | date |  |
| `customFields` | array<object> |  |
| `employeeId` | number |  |
| `employeeType` | string |  |
| `externalPayrollId` | string |  |
| `hireDate` | date |  |
| `hourlyRate` | number |  |
| `isIncludedInPayroll` | boolean |  |
| `managerId` | number |  |
| `modifiedOn` | date |  |
| `payrollBusinessUnitId` | number |  |

## Native endpoint

Through the native ServiceTitan API, this operation is `GET payroll/v2/tenant/{{credentials.tenant}}/technicians/:technician/payroll-settings` (base URL `https://{{credentials.baseUrl}}/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-technician-payroll-settings.md) for the provider-specific parameters and requirements.

