# RO App: List Employees



```
GET https://connect.mindcloud.co/v1/universal/rOApp/latest/actions/list-employees
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RO App `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rOApp/latest/actions/list-employees?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rOApp/latest/actions/list-employees?${params}`, {
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
| `sort` | string | no | Defines the sorting order of returned results. Use a field name to sort ascending or prefix it with a minus sign (-) to sort descending. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "avatar": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "first_name": "Ava",
      "hire_date": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "is_active": true,
      "last_name": "Chen",
      "login": "string",
      "notes": "string",
      "phone": "string",
      "position": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatar` | string |  |
| `created_at` | date |  |
| `email` | string |  |
| `first_name` | string |  |
| `hire_date` | date |  |
| `id` | number |  |
| `is_active` | boolean |  |
| `last_name` | string |  |
| `login` | string |  |
| `notes` | string |  |
| `phone` | string |  |
| `position` | string |  |

## Native endpoint

Through the native RO App API, this operation is `GET /company/employees` (base URL `https://api.roapp.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-employees.md) for the provider-specific parameters and requirements.

