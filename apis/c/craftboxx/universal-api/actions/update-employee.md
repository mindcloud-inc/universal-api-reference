# Craftboxx: Update Employee

Updates an employee in Craftboxx.

```
PUT https://connect.mindcloud.co/v1/universal/craftboxx/latest/actions/update-employee
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Craftboxx `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/craftboxx/latest/actions/update-employee" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "employeeId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/craftboxx/latest/actions/update-employee', {
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
| `email` | string | no | The employee email address. |
| `employeeId` | number | yes | The Craftboxx employee ID. |
| `firstName` | string | no | Employee first name. |
| `lastName` | string | no | Employee last name. |
| `inactive` | boolean | no | Whether the employee is inactive. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "country": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "first_line": "string",
      "first_name": "Ava",
      "full_name": "Ava Chen",
      "id": 1,
      "inactive": true,
      "interfaces": [
        "string"
      ],
      "last_name": "Chen",
      "locale": "string",
      "planner_changelog_url": "https://example.com",
      "planner_delete_url": "https://example.com",
      "planner_details_url": "https://example.com",
      "planner_edit_url": "https://example.com",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `country` | string | Employee country. |
| `created_at` | date | Creation timestamp. |
| `email` | string | Employee email address. |
| `first_line` | string | Primary display line. |
| `first_name` | string | Employee first name. |
| `full_name` | string | Employee full name. |
| `id` | number | Employee ID. |
| `inactive` | boolean | Whether the employee is inactive. |
| `interfaces` | array<string> | Available interface flags. |
| `last_name` | string | Employee last name. |
| `locale` | string | Employee locale. |
| `planner_changelog_url` | string | Planner changelog URL. |
| `planner_delete_url` | string | Planner delete URL. |
| `planner_details_url` | string | Planner details URL. |
| `planner_edit_url` | string | Planner edit URL. |
| `updated_at` | date | Update timestamp. |

## Native endpoint

Through the native Craftboxx API, this operation is `PUT employees/:employeeId` (base URL `https://api.craftboxx.de`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-employee.md) for the provider-specific parameters and requirements.

