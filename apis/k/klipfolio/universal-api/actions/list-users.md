# Klipfolio: List Users

Retrieves a list of users from Klipfolio.

```
GET https://connect.mindcloud.co/v1/universal/klipfolio/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Klipfolio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/klipfolio/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/klipfolio/latest/actions/list-users?${params}`, {
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
      "date_last_login": "string",
      "email": "ava@example.com",
      "first_name": "Ava",
      "id": "string",
      "isActivated": true,
      "last_name": "Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date_last_login` | string |  |
| `email` | string |  |
| `first_name` | string |  |
| `id` | string |  |
| `isActivated` | boolean |  |
| `last_name` | string |  |

## Native endpoint

Through the native Klipfolio API, this operation is `GET /users` (base URL `https://app.klipfolio.com/api/1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

