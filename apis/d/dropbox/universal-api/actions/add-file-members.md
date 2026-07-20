# Dropbox: Add File Members

Adds members to a shared file in Dropbox.

```
POST https://connect.mindcloud.co/v1/universal/dropbox/latest/actions/add-file-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dropbox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dropbox/latest/actions/add-file-members" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "/Codex Dropbox Fixtures/share-target.txt",
  "memberEmails[]": "apps+dropbox-collab@mindcloud.co"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dropbox/latest/actions/add-file-members', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "/Codex Dropbox Fixtures/share-target.txt",
    "memberEmails[]": "apps+dropbox-collab@mindcloud.co"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file` | string | yes | Path or ID of the file to share. Example: `/Codex Dropbox Fixtures/share-target.txt`. |
| `memberEmails[]` | array<string> | yes | Email addresses to invite to the file. Example: `apps+dropbox-collab@mindcloud.co`. |
| `customMessage` | string | no | Optional message included with the invite. Example: `Please review this file.`. |
| `quiet` | boolean | no | When true, suppresses notification emails when possible. Example: `false`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accessLevel` | string | no | Access level to grant to the invited members. Example: `viewer`. |
| `addMessageAsComment` | boolean | no | Add the custom message as a comment on the file. Example: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "invitationSignature": [
        "string"
      ],
      "member": {
        "email": "ava@example.com",
        "tag": "string"
      },
      "result": {
        "success": {
          "tag": "string"
        },
        "tag": "string"
      },
      "sckeySha1": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `invitationSignature[]` | string |  |
| `member.email` | string |  |
| `member.tag` | string |  |
| `result.success.tag` | string |  |
| `result.tag` | string |  |
| `sckeySha1` | string |  |

## Native endpoint

Through the native Dropbox API, this operation is `POST /sharing/add_file_member` (base URL `https://api.dropboxapi.com/2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-file-members.md) for the provider-specific parameters and requirements.

