# Outlook: List Mail Folders

Retrieves mail folders from an Outlook mailbox.

```
GET https://connect.mindcloud.co/v1/universal/outlook/latest/actions/list-mail-folders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Outlook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/outlook/latest/actions/list-mail-folders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/outlook/latest/actions/list-mail-folders?${params}`, {
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

Through the native Outlook API, this operation is `GET /me/mailFolders` (base URL `https://graph.microsoft.com/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-mail-folders.md) for the provider-specific parameters and requirements.

