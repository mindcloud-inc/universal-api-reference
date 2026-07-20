# Poodll: Get Users By Field

Finds users in Poodll by a specific field.

```
GET https://connect.mindcloud.co/v1/universal/poodll/latest/actions/get-users-by-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Poodll `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/poodll/latest/actions/get-users-by-field?connectionId=$CONNECTION_ID&field=string&values%5B%5D=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "field": "string",
  "values[]": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/poodll/latest/actions/get-users-by-field?${params}`, {
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
| `field` | string | yes |  |
| `values[]` | array<string> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "firstname": "Ava",
      "fullname": "Ava Chen",
      "id": 1,
      "lastname": "Chen",
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
| `firstname` | string |  |
| `fullname` | string |  |
| `id` | number |  |
| `lastname` | string |  |
| `username` | string |  |

## Native endpoint

Through the native Poodll API, this operation is `POST {{credentials.baseUrl}}/webservice/rest/server.php` (base URL `{{credentials.baseUrl}}/webservice/rest/server.php`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-users-by-field.md) for the provider-specific parameters and requirements.

