# Kladana: List Employees

Lists employees in your Kladana account.

```
GET https://connect.mindcloud.co/v1/universal/kladana/latest/actions/list-employees
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kladana `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kladana/latest/actions/list-employees?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kladana/latest/actions/list-employees?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "created": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "fullName": "Ava Chen",
      "group": {},
      "id": "string",
      "login": "string",
      "meta": {},
      "name": "Ava Chen",
      "owner": {},
      "phone": "string",
      "position": "string",
      "uid": "string",
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean | Whether the employee is archived. |
| `created` | date | Creation timestamp. |
| `email` | string | Employee email address. |
| `fullName` | string | Employee full name. |
| `group` | object | Group reference. |
| `id` | string | Employee UUID. |
| `login` | string | Employee login. |
| `meta` | object | Kladana metadata reference. |
| `name` | string | Employee display name. |
| `owner` | object | Owner reference. |
| `phone` | string | Employee phone number. |
| `position` | string | Employee position. |
| `uid` | string | Employee user identifier. |
| `updated` | date | Last update timestamp. |

## Native endpoint

Through the native Kladana API, this operation is `GET /entity/employee` (base URL `https://api.kladana.com/api/remap/1.2`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-employees.md) for the provider-specific parameters and requirements.

