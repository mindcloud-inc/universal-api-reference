# GoCanvas: Create User



```
POST https://connect.mindcloud.co/v1/universal/goCanvas/latest/actions/create-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GoCanvas `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/goCanvas/latest/actions/create-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "firstName": "Ava",
  "lastName": "Chen",
  "email": "ava@example.com",
  "departmentRole": "department_admin"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/goCanvas/latest/actions/create-user', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "firstName": "Ava",
    "lastName": "Chen",
    "email": "ava@example.com",
    "departmentRole": "department_admin"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `firstName` | string | yes |  |
| `lastName` | string | yes |  |
| `email` | string | yes |  |
| `departmentId` | number | no | Required when Departments are enabled for the GoCanvas company. |
| `departmentRole` | list<string> | yes | One of: `department_admin`, `department_designer`, `department_dispatcher`, `department_reporter`, `department_user`. |
| `accountRole` | list<string> | no | Only used when Departments are enabled. Leave unset when no account-wide role should be assigned. One of: `account_admin`, `account_reporter`. |
| `password` | string | no | Must meet the company password policy. If omitted, GoCanvas generates a password and sends a setup email unless Skip Welcome Email is enabled. |
| `phone` | string | no |  |
| `skipWelcomeEmail` | boolean | no | Default: `false`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native GoCanvas API returns.

## Native endpoint

Through the native GoCanvas API, this operation is `POST /users` (base URL `https://www.gocanvas.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-user.md) for the provider-specific parameters and requirements.

