# Zoho Mail: Get Folder

Retrieves a folder from Zoho Mail.

```
GET https://connect.mindcloud.co/v1/universal/zohoMail/latest/actions/get-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Mail `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoMail/latest/actions/get-folder?connectionId=$CONNECTION_ID&accountId=3048445000000008002&folderId=3048445000000008014" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "3048445000000008002",
  "folderId": "3048445000000008014"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoMail/latest/actions/get-folder?${params}`, {
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
| `accountId` | string | yes | Account identifier returned by List Accounts. Example: `3048445000000008002`. |
| `folderId` | string | yes | Folder identifier returned by List Folders. Example: `3048445000000008014`. |

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

Through the native Zoho Mail API, this operation is `GET /accounts/:accountId/folders/:folderId` (base URL `https://mail.zoho.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-folder.md) for the provider-specific parameters and requirements.

