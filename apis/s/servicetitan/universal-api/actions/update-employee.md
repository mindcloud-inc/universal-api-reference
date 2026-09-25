# ServiceTitan: Update Employee

Updates an existing employee in ServiceTitan.

```
PUT https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/update-employee
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ServiceTitan `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/update-employee" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "email": "ava@example.com",
  "accountCreationMethod": "string",
  "roleId": 1,
  "positions[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/servicetitan/latest/actions/update-employee', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "email": "ava@example.com",
    "accountCreationMethod": "string",
    "roleId": 1,
    "positions[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customFields[].typeId` | number | no |  |
| `name` | string | yes |  |
| `customFields[].name` | string | no |  |
| `mobilePhoneNumber` | string | no |  |
| `customFields[].value` | string | no |  |
| `phoneNumber` | string | no |  |
| `email` | string | yes |  |
| `login` | string | no |  |
| `password` | string | no |  |
| `accountCreationMethod` | list<string> | yes |  |
| `businessUnitId` | number | no |  |
| `roleId` | number | yes |  |
| `positions[]` | array<string> | yes |  |
| `aadUserId` | string | no |  |
| `customFields[]` | array | no |  |
| `id` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ServiceTitan API returns.

## Native endpoint

Through the native ServiceTitan API, this operation is `PATCH settings/v2/tenant/{{credentials.tenant}}/employees/:id` (base URL `https://{{credentials.baseUrl}}/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-employee.md) for the provider-specific parameters and requirements.

