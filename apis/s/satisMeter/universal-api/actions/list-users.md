# SatisMeter: List Users



```
GET https://connect.mindcloud.co/v1/universal/satisMeter/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SatisMeter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/satisMeter/latest/actions/list-users?connectionId=$CONNECTION_ID&project=61fce0adea447e24ec27d606" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "project": "61fce0adea447e24ec27d606"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/satisMeter/latest/actions/list-users?${params}`, {
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
| `project` | string | yes | Project ID. Example: `61fce0adea447e24ec27d606`. |
| `userId` | string | no | Filter by a specific user ID. Example: `1234`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "users": [
        {
          "created": "2026-05-07T12:00:00.000Z",
          "email": "ava@example.com",
          "events": [
            {}
          ],
          "id": "string",
          "lastSeen": "2026-05-07T12:00:00.000Z",
          "name": "Ava Chen",
          "project": "string",
          "traits": {
            "createdAt": "2026-05-07T12:00:00.000Z",
            "email": "ava@example.com",
            "name": "Ava Chen"
          },
          "userId": "string"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `users` | array<object> | Matched users for the project and optional filters. |
| `users[].created` | date | User creation timestamp. |
| `users[].email` | string | User email. |
| `users[].events` | array<object> | Tracked events for the user. |
| `users[].id` | string | SatisMeter internal user ID. |
| `users[].lastSeen` | date | Most recent activity timestamp. |
| `users[].name` | string | User display name. |
| `users[].project` | string | Project ID. |
| `users[].traits` | object | User traits stored in SatisMeter. |
| `users[].traits.createdAt` | date | User creation timestamp stored as a trait when provided. |
| `users[].traits.email` | string | User email stored as a trait when provided. |
| `users[].traits.name` | string | User name stored as a trait when provided. |
| `users[].userId` | string | External user ID. |

## Native endpoint

Through the native SatisMeter API, this operation is `GET /api/users` (base URL `https://app.satismeter.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

