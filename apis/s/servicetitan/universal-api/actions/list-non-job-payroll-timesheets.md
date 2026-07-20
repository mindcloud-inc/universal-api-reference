# ServiceTitan: List Non-Job Payroll Timesheets

Retrieves non-job payroll timesheets from ServiceTitan.

```
GET https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/list-non-job-payroll-timesheets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServiceTitan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/list-non-job-payroll-timesheets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/list-non-job-payroll-timesheets?${params}`, {
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
| `active` | list | no | Default: `Any`. |
| `employeeId` | number | no |  |
| `pageSize` | number | no | Default: `500`. |
| `employeeType` | list | no | Default: `Technician`. Example: `Technician/Employee`. |
| `createdBefore` | string | no |  |
| `createdOnOrAfter` | string | no |  |
| `modifiedOnOrAfter` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ServiceTitan API returns.

## Native endpoint

Through the native ServiceTitan API, this operation is `GET payroll/v2/tenant/{{credentials.tenant}}/non-job-timesheets` (base URL `https://{{credentials.baseUrl}}/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-non-job-payroll-timesheets.md) for the provider-specific parameters and requirements.

