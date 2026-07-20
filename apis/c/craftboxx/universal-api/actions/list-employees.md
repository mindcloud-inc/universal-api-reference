# Craftboxx: List Employees

Returns employees from Craftboxx.

```
GET https://connect.mindcloud.co/v1/universal/craftboxx/latest/actions/list-employees
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Craftboxx `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/craftboxx/latest/actions/list-employees?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/craftboxx/latest/actions/list-employees?${params}`, {
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
| `q` | string | no | Search employees by a broad Craftboxx query string. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "city": "string",
      "color": "string",
      "contrast_color": "string",
      "country": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "department": "string",
      "driver_license": true,
      "email": "ava@example.com",
      "first_line": "string",
      "first_name": "Ava",
      "full_name": "Ava Chen",
      "group_id": 1,
      "holidays_overtake_balances": true,
      "holidays_per_year": 1,
      "icon": "string",
      "id": 1,
      "inactive": true,
      "info": "string",
      "initials": "string",
      "interfaces": [
        "string"
      ],
      "last_name": "Chen",
      "locale": "string",
      "mobile": "string",
      "number": "string",
      "phone": "string",
      "picture_is_avatar": true,
      "planner_changelog_url": "https://example.com",
      "planner_delete_url": "https://example.com",
      "planner_details_url": "https://example.com",
      "planner_edit_url": "https://example.com",
      "position": "string",
      "skills": "string",
      "sort_order": 1,
      "street": "string",
      "timezone": "string",
      "truck_license": true,
      "updated_at": "2026-05-07T12:00:00.000Z",
      "zip": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `city` | string | Employee city |
| `color` | string | Employee color |
| `contrast_color` | string | Contrast color |
| `country` | string | Employee country |
| `created_at` | date | Employee creation timestamp |
| `department` | string | Employee department |
| `driver_license` | boolean | Whether the employee has a driver license |
| `email` | string | Employee email address |
| `first_line` | string | Primary display line |
| `first_name` | string | Employee first name |
| `full_name` | string | Employee full name |
| `group_id` | number | Employee group ID |
| `holidays_overtake_balances` | boolean | Whether holiday balances overtake automatically |
| `holidays_per_year` | number | Annual holiday allowance |
| `icon` | string | Employee icon |
| `id` | number | Employee ID |
| `inactive` | boolean | Whether the employee is inactive |
| `info` | string | Additional employee info |
| `initials` | string | Employee initials |
| `interfaces` | array<string> | Available interface flags |
| `last_name` | string | Employee last name |
| `locale` | string | Employee locale |
| `mobile` | string | Employee mobile phone |
| `number` | string | Employee number |
| `phone` | string | Employee landline phone |
| `picture_is_avatar` | boolean | Whether the picture is an avatar |
| `planner_changelog_url` | string | Planner changelog URL |
| `planner_delete_url` | string | Planner delete URL |
| `planner_details_url` | string | Planner details URL |
| `planner_edit_url` | string | Planner edit URL |
| `position` | string | Employee position |
| `skills` | string | Employee skills |
| `sort_order` | number | Employee sort order |
| `street` | string | Employee street |
| `timezone` | string | Employee timezone |
| `truck_license` | boolean | Whether the employee has a truck license |
| `updated_at` | date | Employee update timestamp |
| `zip` | string | Employee ZIP code |

## Native endpoint

Through the native Craftboxx API, this operation is `GET employees` (base URL `https://api.craftboxx.de`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-employees.md) for the provider-specific parameters and requirements.

