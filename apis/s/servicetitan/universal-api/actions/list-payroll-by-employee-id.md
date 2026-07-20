# ServiceTitan: List Payroll by Employee ID

Retrieves payrolls from ServiceTitan for an employee.

```
GET https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/list-payroll-by-employee-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServiceTitan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/list-payroll-by-employee-id?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/list-payroll-by-employee-id?${params}`, {
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
| `status` | list | no | Return items of the specified payroll status Values: [Pending, Expired, Approved, Paid, Locked] |
| `active` | list | no | What kind of items should be returned (only active items will be returned by default) Values: [True, Any, False] Default: `Any`. |
| `employeeID` | number | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ServiceTitan API returns.

## Native endpoint

Through the native ServiceTitan API, this operation is `GET payroll/v2/tenant/{{credentials.tenant}}/employees/:employeeID/payrolls` (base URL `https://{{credentials.baseUrl}}/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-payroll-by-employee-id.md) for the provider-specific parameters and requirements.

