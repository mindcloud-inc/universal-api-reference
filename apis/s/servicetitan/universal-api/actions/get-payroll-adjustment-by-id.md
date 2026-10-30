# ServiceTitan: Get Payroll Adjustment By Id

Retrieves a payroll adjustment from ServiceTitan by ID.

```
GET https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/get-payroll-adjustment-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServiceTitan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/get-payroll-adjustment-by-id?connectionId=$CONNECTION_ID&id=1&employeeType=Employee" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1",
  "employeeType": "Employee"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/get-payroll-adjustment-by-id?${params}`, {
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
| `id` | number | yes |  |
| `employeeType` | list<string> | yes | One of: `Employee`, `Technician`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "activityCodeId": 1,
      "amount": 1,
      "businessUnitId": 1,
      "createdOn": "2026-05-07T12:00:00.000Z",
      "employeeId": 1,
      "employeeType": "string",
      "hours": 1,
      "id": 1,
      "invoiceId": 1,
      "memo": "string",
      "modifiedOn": "2026-05-07T12:00:00.000Z",
      "postedOn": "2026-05-07T12:00:00.000Z",
      "quantity": 1,
      "rate": 1,
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `activityCodeId` | number |  |
| `amount` | number |  |
| `businessUnitId` | number |  |
| `createdOn` | date |  |
| `employeeId` | number |  |
| `employeeType` | string |  |
| `hours` | number |  |
| `id` | number |  |
| `invoiceId` | number |  |
| `memo` | string |  |
| `modifiedOn` | date |  |
| `postedOn` | date |  |
| `quantity` | number |  |
| `rate` | number |  |
| `type` | string |  |

## Native endpoint

Through the native ServiceTitan API, this operation is `GET payroll/v2/tenant/{{credentials.tenant}}/payroll-adjustments/:id` (base URL `https://{{credentials.baseUrl}}/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-payroll-adjustment-by-id.md) for the provider-specific parameters and requirements.

