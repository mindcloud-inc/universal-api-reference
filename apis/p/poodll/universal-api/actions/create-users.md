# Poodll: Create Users

Creates new user accounts in Poodll.

```
POST https://connect.mindcloud.co/v1/universal/poodll/latest/actions/create-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Poodll `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/poodll/latest/actions/create-users" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "users[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/poodll/latest/actions/create-users', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "users[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `users[]` | array<object> | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
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
| `id` | number |  |
| `username` | string |  |

## Native endpoint

Through the native Poodll API, this operation is `POST {{credentials.baseUrl}}/webservice/rest/server.php` (base URL `{{credentials.baseUrl}}/webservice/rest/server.php`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-users.md) for the provider-specific parameters and requirements.

