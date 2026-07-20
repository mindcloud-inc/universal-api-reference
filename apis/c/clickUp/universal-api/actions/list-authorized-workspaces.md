# ClickUp: List Authorized Workspaces

View the Workspaces available to the authenticated user.

```
GET https://connect.mindcloud.co/v1/universal/clickUp/latest/actions/list-authorized-workspaces
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClickUp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clickUp/latest/actions/list-authorized-workspaces?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clickUp/latest/actions/list-authorized-workspaces?${params}`, {
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
      "avatar": "string",
      "color": "string",
      "id": "string",
      "members": [
        {
          "user": {
            "color": "string",
            "customRole": "string",
            "dateInvited": "2026-05-07T12:00:00.000Z",
            "dateJoined": "2026-05-07T12:00:00.000Z",
            "email": "ava@example.com",
            "id": 1,
            "initials": "string",
            "lastActive": "2026-05-07T12:00:00.000Z",
            "profilePicture": "string",
            "role": 1,
            "username": "Ava Chen"
          }
        }
      ],
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatar` | string |  |
| `color` | string |  |
| `id` | string |  |
| `members[].user.color` | string |  |
| `members[].user.customRole` | string |  |
| `members[].user.dateInvited` | date |  |
| `members[].user.dateJoined` | date |  |
| `members[].user.email` | string |  |
| `members[].user.id` | number |  |
| `members[].user.initials` | string |  |
| `members[].user.lastActive` | date |  |
| `members[].user.profilePicture` | string |  |
| `members[].user.role` | number |  |
| `members[].user.username` | string |  |
| `name` | string |  |

## Native endpoint

Through the native ClickUp API, this operation is `GET team` (base URL `https://api.clickup.com/api/v2/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-authorized-workspaces.md) for the provider-specific parameters and requirements.

