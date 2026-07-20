# Dashform: Get Current User

Retrieves the current user from Dashform.

```
GET https://connect.mindcloud.co/v1/universal/dashform/latest/actions/get-current-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dashform `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dashform/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dashform/latest/actions/get-current-user?${params}`, {
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
      "createdAt": "string",
      "email": "ava@example.com",
      "emailVerified": true,
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string | Account creation timestamp |
| `email` | string | Account email address |
| `emailVerified` | boolean | Whether the email is verified |
| `id` | string | Dashform user identifier |
| `name` | string | Profile display name |

## Native endpoint

Through the native Dashform API, this operation is `GET /api/v1/me` (base URL `https://getaiform.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-user.md) for the provider-specific parameters and requirements.

