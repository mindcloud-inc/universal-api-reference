# Craftboxx: Create Employee

Creates an employee in Craftboxx.

```
POST https://connect.mindcloud.co/v1/universal/craftboxx/latest/actions/create-employee
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Craftboxx `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/craftboxx/latest/actions/create-employee" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "firstName": "Ava",
  "lastName": "Chen",
  "email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/craftboxx/latest/actions/create-employee', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "firstName": "Ava",
    "lastName": "Chen",
    "email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `firstName` | string | yes | Employee first name. |
| `lastName` | string | yes | Employee last name. |
| `email` | string | yes | The employee email address. |

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

Through the native Craftboxx API, this operation is `POST employees` (base URL `https://api.craftboxx.de`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-employee.md) for the provider-specific parameters and requirements.

