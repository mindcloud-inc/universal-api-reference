# ServiceTitan: Create Payroll Adjustment



```
POST https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/create-payroll-adjustment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServiceTitan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/create-payroll-adjustment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "employeeType": "Employee",
  "employeeId": 1,
  "postedOn": "2026-01-15T00:00:00Z"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/create-payroll-adjustment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "employeeType": "Employee",
    "employeeId": 1,
    "postedOn": "2026-01-15T00:00:00Z"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `employeeType` | list<string> | yes | One of: `Employee`, `Technician`. |
| `employeeId` | number | yes | ID of the employee or technician selected by Employee Type. |
| `postedOn` | date | yes | Date and time the adjustment is posted, in UTC. Example: `2026-01-15T00:00:00Z`. |
| `amount` | number | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `memo` | string | no |  |
| `activityCodeId` | number | no |  |
| `invoiceId` | list<number> | no |  |
| `businessUnitId` | list<number> | no |  |
| `hours` | number | no |  |
| `rate` | number | no |  |
| `quantity` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |

## Native endpoint

Through the native ServiceTitan API, this operation is `POST payroll/v2/tenant/{{credentials.tenant}}/payroll-adjustments` (base URL `https://{{credentials.baseUrl}}/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-payroll-adjustment.md) for the provider-specific parameters and requirements.

