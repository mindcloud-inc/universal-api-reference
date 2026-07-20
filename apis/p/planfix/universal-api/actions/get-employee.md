# Planfix: Get Employee

Retrieves an employee from Planfix.

```
GET https://connect.mindcloud.co/v1/universal/planfix/latest/actions/get-employee
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Planfix `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/planfix/latest/actions/get-employee?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/planfix/latest/actions/get-employee?${params}`, {
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
| `id` | number | yes | Planfix employee identifier. |
| `fields` | string | no | Comma-delimited employee fields to return. Default: `id,name,email`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "id": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string |  |
| `id` | number |  |
| `name` | string |  |

## Native endpoint

Through the native Planfix API, this operation is `GET /user/:id` (base URL `{{credentials.accountBaseUrl}}/rest`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-employee.md) for the provider-specific parameters and requirements.

