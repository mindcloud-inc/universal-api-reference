# ServiceTitan: Update Technician Payroll Settings



```
PUT https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/update-technician-payroll-settings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServiceTitan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/update-technician-payroll-settings" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "technician": 1,
  "hourlyRate": 1,
  "customFields[].typeId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/update-technician-payroll-settings', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "technician": 1,
    "hourlyRate": 1,
    "customFields[].typeId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `technician` | number | yes | The ServiceTitan technician ID. |
| `externalPayrollId` | string | no | Optional identifier from the external payroll system. |
| `hourlyRate` | number | yes | Hourly rate for the technician payroll settings. |
| `managerId` | number | no | Optional manager employee ID. |
| `hireDate` | date | no | Optional hire date and time. |
| `isIncludedInPayroll` | boolean | no | Whether the technician is included in payroll processing. |
| `customFields[].typeId` | number | yes | Custom payroll field definition ID. |
| `customFields[].value` | string | no | Optional custom payroll field value. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customFields[]` | array<object> | no | Optional custom payroll-field values to update for the technician. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "employeeId": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `employeeId` | number | Employee ID associated with the updated technician payroll settings. |

## Native endpoint

Through the native ServiceTitan API, this operation is `PUT payroll/v2/tenant/{{credentials.tenant}}/technicians/:technician/payroll-settings` (base URL `https://{{credentials.baseUrl}}/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-technician-payroll-settings.md) for the provider-specific parameters and requirements.

