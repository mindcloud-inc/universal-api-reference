# Planday: Deactivate Employee

Deactivates an existing employee in Planday.

```
PUT https://connect.mindcloud.co/v1/universal/planday/latest/actions/deactivate-employee
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Planday `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/planday/latest/actions/deactivate-employee" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "employeeId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/planday/latest/actions/deactivate-employee', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "employeeId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `date` | string | no |  |
| `employeeId` | number | yes |  |
| `keepShifts` | boolean | no |  |
| `reason` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Planday API returns.

## Native endpoint

Through the native Planday API, this operation is `PUT /hr/v1.0/employees/deactivate/:employeeId` (base URL `https://openapi.planday.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/deactivate-employee.md) for the provider-specific parameters and requirements.

