# Pachca (Admin): List Chat Members

Retrieves chat members from the Pachca Admin API.

```
GET https://connect.mindcloud.co/v1/universal/pachcaAdmin/latest/actions/list-chat-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pachca (Admin) `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pachcaAdmin/latest/actions/list-chat-members?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pachcaAdmin/latest/actions/list-chat-members?${params}`, {
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
| `id` | number | yes | The Pachca chat ID. |
| `role` | string | no |  |
| `limit` | number | no |  |
| `cursor` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "bot": true,
          "createdAt": "string",
          "department": {},
          "email": "ava@example.com",
          "firstName": "Ava",
          "id": 1,
          "imageUrl": {},
          "inviteStatus": "string",
          "lastActivityAt": "string",
          "lastName": "Chen",
          "nickname": "Ava Chen",
          "phoneNumber": {},
          "role": "string",
          "sso": true,
          "suspended": true,
          "timeZone": "string",
          "title": {},
          "userStatus": {}
        }
      ],
      "meta": {
        "paginate": {
          "nextPage": "string"
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].bot` | boolean |  |
| `data[].createdAt` | string |  |
| `data[].department` | object |  |
| `data[].email` | string |  |
| `data[].firstName` | string |  |
| `data[].id` | number |  |
| `data[].imageUrl` | object |  |
| `data[].inviteStatus` | string |  |
| `data[].lastActivityAt` | string |  |
| `data[].lastName` | string |  |
| `data[].nickname` | string |  |
| `data[].phoneNumber` | object |  |
| `data[].role` | string |  |
| `data[].sso` | boolean |  |
| `data[].suspended` | boolean |  |
| `data[].timeZone` | string |  |
| `data[].title` | object |  |
| `data[].userStatus` | object |  |
| `meta.paginate.nextPage` | string |  |

## Native endpoint

Through the native Pachca (Admin) API, this operation is `GET /chats/:id/members` (base URL `https://api.pachca.com/api/shared/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-chat-members.md) for the provider-specific parameters and requirements.

