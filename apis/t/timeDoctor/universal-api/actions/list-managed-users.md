# Time Doctor: List Managed Users

Retrieves managed users from Time Doctor.

```
GET https://connect.mindcloud.co/v1/universal/timeDoctor/latest/actions/list-managed-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Time Doctor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/timeDoctor/latest/actions/list-managed-users?connectionId=$CONNECTION_ID&userId=me" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "me"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/timeDoctor/latest/actions/list-managed-users?${params}`, {
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
| `userId` | string | yes | ID of the manager or user to inspect. Use `me` for the caller. Default: `me`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "hiredAt": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "name": "Ava Chen",
      "onlyProjectIds": [
        "string"
      ],
      "profileTimezone": "string",
      "role": "string",
      "status": "string",
      "timezone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `createdAt` | date |  |
| `email` | string |  |
| `hiredAt` | date |  |
| `id` | string |  |
| `name` | string |  |
| `onlyProjectIds` | array<string> |  |
| `profileTimezone` | string |  |
| `role` | string |  |
| `status` | string |  |
| `timezone` | string |  |

## Native endpoint

Through the native Time Doctor API, this operation is `GET /api/1.0/users/:userId/managed` (base URL `https://api2.timedoctor.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-managed-users.md) for the provider-specific parameters and requirements.

