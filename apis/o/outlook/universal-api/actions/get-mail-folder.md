# Outlook: Get Mail Folder

Retrieves an Outlook mail folder by folder ID.

```
GET https://connect.mindcloud.co/v1/universal/outlook/latest/actions/get-mail-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Outlook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/outlook/latest/actions/get-mail-folder?connectionId=$CONNECTION_ID&folderId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "folderId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/outlook/latest/actions/get-mail-folder?${params}`, {
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
| `folderId` | string | yes | Microsoft Graph ID or well-known folder name, such as inbox, for the Outlook mail folder. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "childFolderCount": 1,
      "displayName": "Ava Chen",
      "id": "string",
      "isHidden": true,
      "parentFolderId": "string",
      "totalItemCount": 1,
      "unreadItemCount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `childFolderCount` | number | Number of immediate child folders. |
| `displayName` | string | Folder display name. |
| `id` | string | Microsoft Graph mail folder ID. |
| `isHidden` | boolean | Whether the folder is hidden. |
| `parentFolderId` | string | ID of the folder's parent folder. |
| `totalItemCount` | number | Total number of items in the folder. |
| `unreadItemCount` | number | Number of unread items in the folder. |

## Native endpoint

Through the native Outlook API, this operation is `GET /me/mailFolders/:folderId` (base URL `https://graph.microsoft.com/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-mail-folder.md) for the provider-specific parameters and requirements.

