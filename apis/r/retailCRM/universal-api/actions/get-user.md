# retailCRM: Get User

Retrieves a user from retailCRM by ID.

```
GET https://connect.mindcloud.co/v1/universal/retailCRM/latest/actions/get-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a retailCRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/retailCRM/latest/actions/get-user?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/retailCRM/latest/actions/get-user?${params}`, {
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
| `id` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "createdAt": "string",
      "email": "ava@example.com",
      "firstName": "Ava",
      "groups": [
        {
          "code": "string",
          "id": 1,
          "name": "Ava Chen"
        }
      ],
      "id": 1,
      "isAdmin": true,
      "isManager": true,
      "lastOnline": "string",
      "mgUserId": 1,
      "online": true,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `createdAt` | string |  |
| `email` | string |  |
| `firstName` | string |  |
| `groups[].code` | string |  |
| `groups[].id` | number |  |
| `groups[].name` | string |  |
| `id` | number |  |
| `isAdmin` | boolean |  |
| `isManager` | boolean |  |
| `lastOnline` | string |  |
| `mgUserId` | number |  |
| `online` | boolean |  |
| `status` | string |  |

## Native endpoint

Through the native retailCRM API, this operation is `GET /users/:id` (base URL `{{credentials.accountUrl}}/api/v5`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user.md) for the provider-specific parameters and requirements.

