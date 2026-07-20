# SupportBee: List Users

Retrieves users and customer groups from SupportBee.

```
GET https://connect.mindcloud.co/v1/universal/supportBee/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SupportBee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/supportBee/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/supportBee/latest/actions/list-users?${params}`, {
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
| `withInvited` | boolean | no | If true, include invited users. |
| `withRoles` | string | no | Include role information when requested. |
| `type` | string | no | Filter by user type. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "users": [
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `users[]` | array<object> |  |
| `users[].agent` | boolean |  |
| `users[].canMembersAccessGroupTickets` | object |  |
| `users[].email` | string |  |
| `users[].emailDomains[]` | array |  |
| `users[].firstName` | string |  |
| `users[].id` | number |  |
| `users[].lastName` | string |  |
| `users[].membersCount` | number |  |
| `users[].name` | string |  |
| `users[].picture` | object |  |
| `users[].picture.thumb128` | string |  |
| `users[].picture.thumb20` | string |  |
| `users[].picture.thumb24` | string |  |
| `users[].picture.thumb32` | string |  |
| `users[].picture.thumb48` | string |  |
| `users[].picture.thumb64` | string |  |
| `users[].role` | string |  |
| `users[].teams[]` | array |  |
| `users[].twoFactorAuthenticationEnabled` | boolean |  |
| `users[].type` | string |  |

## Native endpoint

Through the native SupportBee API, this operation is `GET /users` (base URL `https://{{credentials.company}}.supportbee.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

