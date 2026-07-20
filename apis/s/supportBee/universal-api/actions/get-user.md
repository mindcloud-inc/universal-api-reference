# SupportBee: Get User

Retrieves a user or customer group from SupportBee.

```
GET https://connect.mindcloud.co/v1/universal/supportBee/latest/actions/get-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SupportBee `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/supportBee/latest/actions/get-user?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/supportBee/latest/actions/get-user?${params}`, {
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
| `id` | number | yes | SupportBee user ID. |
| `maxTickets` | number | no | Maximum number of related tickets to include. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "user": {
        "activeTicketsCount": 1,
        "agent": true,
        "canMembersAccessGroupTickets": {},
        "customerGroups": [
          [
            "string"
          ]
        ],
        "email": "ava@example.com",
        "emailDomains": [
          [
            "ava@example.com"
          ]
        ],
        "firstName": "Ava",
        "id": 1,
        "lastName": "Chen",
        "membersCount": 1,
        "name": "Ava Chen",
        "picture": {
          "thumb128": "string",
          "thumb20": "string",
          "thumb24": "string",
          "thumb32": "string",
          "thumb48": "string",
          "thumb64": "string"
        },
        "role": "string",
        "signature": "string",
        "teams": [
          [
            "string"
          ]
        ],
        "tickets": [
          [
            "string"
          ]
        ],
        "twoFactorAuthenticationEnabled": true,
        "type": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `user` | object |  |
| `user.activeTicketsCount` | number |  |
| `user.agent` | boolean |  |
| `user.canMembersAccessGroupTickets` | object |  |
| `user.customerGroups[]` | array |  |
| `user.email` | string |  |
| `user.emailDomains[]` | array |  |
| `user.firstName` | string |  |
| `user.id` | number |  |
| `user.lastName` | string |  |
| `user.membersCount` | number |  |
| `user.name` | string |  |
| `user.picture` | object |  |
| `user.picture.thumb128` | string |  |
| `user.picture.thumb20` | string |  |
| `user.picture.thumb24` | string |  |
| `user.picture.thumb32` | string |  |
| `user.picture.thumb48` | string |  |
| `user.picture.thumb64` | string |  |
| `user.role` | string |  |
| `user.signature` | string |  |
| `user.teams[]` | array |  |
| `user.tickets[]` | array |  |
| `user.twoFactorAuthenticationEnabled` | boolean |  |
| `user.type` | string |  |

## Native endpoint

Through the native SupportBee API, this operation is `GET /users/:id` (base URL `https://{{credentials.company}}.supportbee.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user.md) for the provider-specific parameters and requirements.

