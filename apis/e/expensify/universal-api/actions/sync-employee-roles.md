# Expensify: Sync Employee Roles

Updates employee roles in Expensify.

```
PUT https://connect.mindcloud.co/v1/universal/expensify/latest/actions/sync-employee-roles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Expensify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/expensify/latest/actions/sync-employee-roles" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "employeesJson": [
    {
      "role": "user",
      "policyID": "0000000000000000",
      "employeeID": "wizard-stage4-invalid-001",
      "managerEmail": "apps@mindcloud.co",
      "employeeEmail": "wizard.invalid1@mindcloud.co"
    }
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/expensify/latest/actions/sync-employee-roles', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "employeesJson": [{"role":"user","policyID":"0000000000000000","employeeID":"wizard-stage4-invalid-001","managerEmail":"apps@mindcloud.co","employeeEmail":"wizard.invalid1@mindcloud.co"}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `employeesJson` | string | yes | JSON array of employee objects for the Advanced Employee Updater request-mode feed. Default: `[{"role":"user","policyID":"0000000000000000","employeeID":"wizard-stage4-invalid-001","managerEmail":"apps@mindcloud.co","employeeEmail":"wizard.invalid1@mindcloud.co"}]`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dry-run": true,
      "email": "ava@example.com",
      "reason": "string",
      "requestID": "string",
      "responseCode": 1,
      "updatedEmployeesCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dry-run` | boolean |  |
| `email` | string |  |
| `reason` | string |  |
| `requestID` | string |  |
| `responseCode` | number |  |
| `updatedEmployeesCount` | number |  |

## Native endpoint

Through the native Expensify API, this operation is `POST ExpensifyIntegrations` (base URL `https://integrations.expensify.com/Integration-Server/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/sync-employee-roles.md) for the provider-specific parameters and requirements.

