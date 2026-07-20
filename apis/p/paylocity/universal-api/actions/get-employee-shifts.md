# Paylocity: Get Employee Shifts



```
GET https://connect.mindcloud.co/v1/universal/paylocity/latest/actions/get-employee-shifts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Paylocity `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/paylocity/latest/actions/get-employee-shifts?connectionId=$CONNECTION_ID&companyId=string&employeeId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "companyId": "string",
  "employeeId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/paylocity/latest/actions/get-employee-shifts?${params}`, {
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
| `include` | string | no | breaks, segments, note |
| `filter` | string | no | - fields: startDateTime, positionKey - operators: eq, in, lt, gt, le, ge, and, or - example: startDateTime gt '2024-12-01' and startDateTime le '2025-01-25' |
| `companyId` | string | yes |  |
| `employeeId` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Paylocity API returns.

## Native endpoint

Through the native Paylocity API, this operation is `GET apiHub/scheduling/v1/companies/:companyId/employees/:employeeId/shifts` (base URL `{{credentials.connection}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-employee-shifts.md) for the provider-specific parameters and requirements.

