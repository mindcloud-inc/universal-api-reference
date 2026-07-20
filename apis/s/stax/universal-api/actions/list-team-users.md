# Stax: List Team Users

Retrieves team users from Stax.

```
GET https://connect.mindcloud.co/v1/universal/stax/latest/actions/list-team-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stax `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stax/latest/actions/list-team-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stax/latest/actions/list-team-users?${params}`, {
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
      "id": "string",
      "name": "Ava Chen",
      "teamAdmin": true,
      "teamEnabled": true,
      "teamRole": "string",
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string | Creation timestamp. |
| `email` | string | Team user email address. |
| `id` | string | Team user identifier. |
| `name` | string | Team user display name. |
| `teamAdmin` | boolean | Whether the user is a team admin. |
| `teamEnabled` | boolean | Whether the team user is active. |
| `teamRole` | string | Role assigned within the team. |
| `updatedAt` | string | Last update timestamp. |

## Native endpoint

Through the native Stax API, this operation is `GET /team/user` (base URL `https://apiprod.fattlabs.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-team-users.md) for the provider-specific parameters and requirements.

