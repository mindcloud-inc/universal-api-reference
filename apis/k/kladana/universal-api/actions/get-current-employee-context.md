# Kladana: Get Current Employee Context

Retrieves current employee context from Kladana.

```
GET https://connect.mindcloud.co/v1/universal/kladana/latest/actions/get-current-employee-context
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kladana `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kladana/latest/actions/get-current-employee-context?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kladana/latest/actions/get-current-employee-context?${params}`, {
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
      "firstName": "Ava",
      "fullName": "Ava Chen",
      "id": "string",
      "lastName": "Chen",
      "login": "string",
      "meta": {},
      "name": "Ava Chen",
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
| `firstName` | string | Employee first name. |
| `fullName` | string | Employee full name. |
| `id` | string | Employee UUID. |
| `lastName` | string | Employee last name. |
| `login` | string | Employee login. |
| `meta` | object | Kladana metadata reference. |
| `name` | string | Employee display name. |
| `phone` | string | Employee phone number. |
| `position` | string | Employee position. |
| `uid` | string | Employee user identifier. |
| `updated` | date | Last update timestamp. |

## Native endpoint

Through the native Kladana API, this operation is `GET /context/employee` (base URL `https://api.kladana.com/api/remap/1.2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-employee-context.md) for the provider-specific parameters and requirements.

