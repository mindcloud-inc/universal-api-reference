# Dolibarr: Get Current User Info

Retrieves the current user's details from Dolibarr.

```
GET https://connect.mindcloud.co/v1/universal/dolibarr/latest/actions/get-current-user-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dolibarr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dolibarr/latest/actions/get-current-user-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dolibarr/latest/actions/get-current-user-info?${params}`, {
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

Through the native Dolibarr API, this operation is `GET /users/info` (base URL `https://mindcloud-dolibarr-0421.with7.dolicloud.com/api/index.php`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-user-info.md) for the provider-specific parameters and requirements.

