# GrooveHQ: Get Current User

Retrieves the current user from GrooveHQ.

```
GET https://connect.mindcloud.co/v1/universal/grooveHQ/latest/actions/get-current-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GrooveHQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/grooveHQ/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/grooveHQ/latest/actions/get-current-user?${params}`, {
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": "string",
      "lastName": "Chen",
      "lastSignInAt": "2026-05-07T12:00:00.000Z",
      "links": {},
      "preferredMailboxId": "string",
      "role": "string",
      "state": "string",
      "subdomain": "string",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | date | User creation timestamp. |
| `email` | string | Current user email. |
| `firstName` | string | Current user first name. |
| `id` | string | Current user identifier. |
| `lastName` | string | Current user last name. |
| `lastSignInAt` | date | Last sign-in timestamp. |
| `links` | object | Provider links for related resources. |
| `preferredMailboxId` | string | Preferred mailbox identifier. |
| `role` | string | Current user role. |
| `state` | string | Current user state. |
| `subdomain` | string | Workspace subdomain. |
| `username` | string | Current user username. |

## Native endpoint

Through the native GrooveHQ API, this operation is `GET /me` (base URL `https://api.groovehq.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-user.md) for the provider-specific parameters and requirements.

