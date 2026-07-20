# Dolibarr: Get User By Login

Retrieves a user from Dolibarr by login.

```
GET https://connect.mindcloud.co/v1/universal/dolibarr/latest/actions/get-user-by-login
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dolibarr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dolibarr/latest/actions/get-user-by-login?connectionId=$CONNECTION_ID&login=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "login": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dolibarr/latest/actions/get-user-by-login?${params}`, {
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
| `login` | string | yes | Dolibarr user login. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "admin": "string",
      "datec": 1,
      "datelastlogin": 1,
      "email": "ava@example.com",
      "employee": "string",
      "entity": "string",
      "firstname": "Ava",
      "id": "string",
      "lastname": "Chen",
      "login": "string",
      "ref": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `admin` | string | Admin flag. |
| `datec` | number | Creation timestamp. |
| `datelastlogin` | number | Last login timestamp. |
| `email` | string | User email address. |
| `employee` | string | Employee flag. |
| `entity` | string | Dolibarr entity id. |
| `firstname` | string | User first name. |
| `id` | string | Dolibarr user id. |
| `lastname` | string | User last name. |
| `login` | string | User login. |
| `ref` | string | Dolibarr user reference. |
| `status` | string | User status. |

## Native endpoint

Through the native Dolibarr API, this operation is `GET /users/login/{login}` (base URL `https://mindcloud-dolibarr-0421.with7.dolicloud.com/api/index.php`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-by-login.md) for the provider-specific parameters and requirements.

