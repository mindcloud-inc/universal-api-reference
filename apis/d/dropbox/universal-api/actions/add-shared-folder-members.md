# Dropbox: Add Shared Folder Members

Adds members to a shared folder in Dropbox.

```
POST https://connect.mindcloud.co/v1/universal/dropbox/latest/actions/add-shared-folder-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dropbox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dropbox/latest/actions/add-shared-folder-members" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sharedFolderId": "845281924530794",
  "memberEmails[]": "apps+dropbox-collab@mindcloud.co"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dropbox/latest/actions/add-shared-folder-members', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sharedFolderId": "845281924530794",
    "memberEmails[]": "apps+dropbox-collab@mindcloud.co"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sharedFolderId` | string | yes | ID of the shared folder to update. Example: `845281924530794`. |
| `memberEmails[]` | array<string> | yes | Email addresses to invite to the shared folder. Example: `apps+dropbox-collab@mindcloud.co`. |
| `accessLevel` | string | no | Access level to grant to each invited member. Example: `viewer`. |
| `quiet` | boolean | no | When true, suppresses notification emails when possible. Example: `false`. |
| `customMessage` | string | no | Optional message included with the invite. Example: `Please review this folder.`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Dropbox API returns.

## Native endpoint

Through the native Dropbox API, this operation is `POST /sharing/add_folder_member` (base URL `https://api.dropboxapi.com/2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-shared-folder-members.md) for the provider-specific parameters and requirements.

