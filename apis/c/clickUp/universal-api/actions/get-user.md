# ClickUp: Get User



```
GET https://connect.mindcloud.co/v1/universal/clickUp/latest/actions/get-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ClickUp `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clickUp/latest/actions/get-user?connectionId=$CONNECTION_ID&teamID=string&userID=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "teamID": "string",
  "userID": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clickUp/latest/actions/get-user?${params}`, {
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
| `includeShared` | boolean | no |  |
| `teamID` | list | yes |  |
| `userID` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "member": {
        "invitedBy": {
          "color": "string",
          "email": "ava@example.com",
          "id": 1,
          "initials": "string",
          "profilePicture": "string",
          "username": "Ava Chen"
        },
        "shared": {
          "folders": [
            "string"
          ],
          "lists": [
            "string"
          ],
          "tasks": [
            "string"
          ]
        },
        "user": {
          "color": "string",
          "customRole": {
            "id": 1,
            "name": "Ava Chen"
          },
          "dateInvited": "string",
          "dateJoined": "string",
          "email": "ava@example.com",
          "id": 1,
          "initials": "string",
          "lastActive": "string",
          "profilePicture": "string",
          "role": 1,
          "username": "Ava Chen"
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
| `member` | object |  |
| `member.invitedBy` | object |  |
| `member.invitedBy.color` | string |  |
| `member.invitedBy.email` | string |  |
| `member.invitedBy.id` | number |  |
| `member.invitedBy.initials` | string |  |
| `member.invitedBy.profilePicture` | string |  |
| `member.invitedBy.username` | string |  |
| `member.shared` | object |  |
| `member.shared.folders` | array |  |
| `member.shared.folders[]` | string |  |
| `member.shared.lists` | array |  |
| `member.shared.lists[]` | string |  |
| `member.shared.tasks` | array |  |
| `member.shared.tasks[]` | string |  |
| `member.user` | object |  |
| `member.user.color` | string |  |
| `member.user.customRole` | object |  |
| `member.user.customRole.id` | number |  |
| `member.user.customRole.name` | string |  |
| `member.user.dateInvited` | string |  |
| `member.user.dateJoined` | string |  |
| `member.user.email` | string |  |
| `member.user.id` | number |  |
| `member.user.initials` | string |  |
| `member.user.lastActive` | string |  |
| `member.user.profilePicture` | string |  |
| `member.user.role` | number |  |
| `member.user.username` | string |  |

## Native endpoint

Through the native ClickUp API, this operation is `GET team/:team_id/user/:user_id` (base URL `https://api.clickup.com/api/v2/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user.md) for the provider-specific parameters and requirements.

