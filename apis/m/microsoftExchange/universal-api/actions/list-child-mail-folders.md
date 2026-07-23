# Microsoft Exchange: List Child Mail Folders

Retrieves child mail folders from Microsoft Exchange.

```
GET https://connect.mindcloud.co/v1/universal/microsoftExchange/latest/actions/list-child-mail-folders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Exchange `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoftExchange/latest/actions/list-child-mail-folders?connectionId=$CONNECTION_ID&mailFolderId=inbox" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "mailFolderId": "inbox"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoftExchange/latest/actions/list-child-mail-folders?${params}`, {
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
| `mailFolderId` | string | yes | Choose the parent mail folder. If you are not sure where to start, choose Inbox. Example: `inbox`. |
| `top` | number | no | Maximum number of child folders to return. Default: `25`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `includeHiddenFolders` | boolean | no | Whether to include hidden child folders in the results. |

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
| `childFolderCount` | number | The number of child folders. |
| `displayName` | string | The child mail folder display name. |
| `id` | string | The child mail folder ID. |
| `isHidden` | boolean | Whether the folder is hidden. |
| `parentFolderId` | string | The parent mail folder ID. |
| `totalItemCount` | number | The total number of items. |
| `unreadItemCount` | number | The number of unread items. |

## Native endpoint

Through the native Microsoft Exchange API, this operation is `GET /v1.0/me/mailFolders/{{mailFolderId}}/childFolders` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-child-mail-folders.md) for the provider-specific parameters and requirements.

