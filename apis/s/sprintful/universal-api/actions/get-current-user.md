# Sprintful: Get Current User

Retrieves the current user from Sprintful.

```
GET https://connect.mindcloud.co/v1/universal/sprintful/latest/actions/get-current-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sprintful `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sprintful/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sprintful/latest/actions/get-current-user?${params}`, {
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
      "data": {
        "email": "ava@example.com",
        "name": "Ava Chen"
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | The current Sprintful user profile. |
| `data.email` | string | The Sprintful user email address. |
| `data.name` | string | The Sprintful user display name. |
| `success` | boolean | Whether the Sprintful request succeeded. |

## Native endpoint

Through the native Sprintful API, this operation is `GET /users/me` (base URL `https://app.sprintful.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-user.md) for the provider-specific parameters and requirements.

