# Poodll: Get Enrolled Users

Retrieves enrolled users from a Poodll course.

```
GET https://connect.mindcloud.co/v1/universal/poodll/latest/actions/get-enrolled-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Poodll `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/poodll/latest/actions/get-enrolled-users?connectionId=$CONNECTION_ID&courseid=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "courseid": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/poodll/latest/actions/get-enrolled-users?${params}`, {
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
| `courseid` | number | yes |  |
| `options[]` | array<object> | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "fullname": "Ava Chen",
      "groups": [
        {}
      ],
      "id": 1,
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string |  |
| `fullname` | string |  |
| `groups` | array<object> |  |
| `id` | number |  |
| `username` | string |  |

## Native endpoint

Through the native Poodll API, this operation is `POST {{credentials.baseUrl}}/webservice/rest/server.php` (base URL `{{credentials.baseUrl}}/webservice/rest/server.php`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-enrolled-users.md) for the provider-specific parameters and requirements.

