# Zoho Mail: Create Folder

Creates a new folder in Zoho Mail.

```
POST https://connect.mindcloud.co/v1/universal/zohoMail/latest/actions/create-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Mail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoMail/latest/actions/create-folder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": "3048445000000008002",
  "folderName": "CodexStageThreeFolder"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoMail/latest/actions/create-folder', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": "3048445000000008002",
    "folderName": "CodexStageThreeFolder"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `accountId` | string | yes | Account identifier returned by List Accounts. Example: `3048445000000008002`. |
| `folderName` | string | yes | Unique folder name to create. Special characters are not allowed. Example: `CodexStageThreeFolder`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `parentFolderId` | string | no | Optional parent folder identifier. Example: `3048445000000008014`. |
| `parentFolderPath` | string | no | Optional parent folder path. Example: `/Inbox`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "folderIcon": "string",
      "folderId": "string",
      "folderName": "Ava Chen",
      "folderType": "string",
      "hide": true,
      "imapAccess": true,
      "isArchived": 1,
      "path": "string",
      "previousFolderId": "string",
      "uri": "string",
      "vw": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `folderIcon` | string | Folder icon |
| `folderId` | string | Folder identifier |
| `folderName` | string | Folder name |
| `folderType` | string | Folder type |
| `hide` | boolean | Folder hidden flag |
| `imapAccess` | boolean | IMAP access flag |
| `isArchived` | number | Folder archived status code |
| `path` | string | Folder path |
| `previousFolderId` | string | Previous folder identifier |
| `uri` | string | Folder API URI |
| `vw` | boolean | Folder visibility flag |

## Native endpoint

Through the native Zoho Mail API, this operation is `POST /accounts/:accountId/folders` (base URL `https://mail.zoho.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-folder.md) for the provider-specific parameters and requirements.

