# Dropbox: List Shared Folder Members

Retrieves members of a shared folder from Dropbox.

```
GET https://connect.mindcloud.co/v1/universal/dropbox/latest/actions/list-shared-folder-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dropbox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dropbox/latest/actions/list-shared-folder-members?connectionId=$CONNECTION_ID&sharedFolderId=845281924530794" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sharedFolderId": "845281924530794"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dropbox/latest/actions/list-shared-folder-members?${params}`, {
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
| `sharedFolderId` | string | yes | ID of the shared folder to inspect. Example: `845281924530794`. |
| `limit` | number | no | Maximum number of members to return. Example: `100`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `actions` | list<string> | no | Optional list of member actions to filter for. Leave blank to return all shared folder members. |
| `cursor` | string | no | Cursor returned by a previous List Shared Folder Members call. Example: `AAFdGEp0n3QAAAAAAAABaQ`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "users": [
        {
          "accessType": {
            "tag": "string"
          },
          "isInherited": true,
          "user": {
            "accountId": "string",
            "displayName": "Ava Chen",
            "email": "ava@example.com",
            "sameTeam": true
          }
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
| `users[].accessType.tag` | string |  |
| `users[].isInherited` | boolean |  |
| `users[].user.accountId` | string |  |
| `users[].user.displayName` | string |  |
| `users[].user.email` | string |  |
| `users[].user.sameTeam` | boolean |  |

## Native endpoint

Through the native Dropbox API, this operation is `POST /sharing/list_folder_members` (base URL `https://api.dropboxapi.com/2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-shared-folder-members.md) for the provider-specific parameters and requirements.

