# Microsoft 365: List Child Mail Folders

Retrieves child mail folders from Microsoft 365.

```
GET https://connect.mindcloud.co/v1/universal/microsoft365/latest/actions/list-child-mail-folders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft 365 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoft365/latest/actions/list-child-mail-folders?connectionId=$CONNECTION_ID&mailFolderId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "mailFolderId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoft365/latest/actions/list-child-mail-folders?${params}`, {
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
| `mailFolderId` | list<string> | yes | Choose the parent mail folder from the folder lookup. If you are not sure where to start, choose Inbox. |
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
      "sizeInBytes": 1,
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
| `childFolderCount` | number |  |
| `displayName` | string |  |
| `id` | string |  |
| `isHidden` | boolean |  |
| `parentFolderId` | string |  |
| `sizeInBytes` | number |  |
| `totalItemCount` | number |  |
| `unreadItemCount` | number |  |

## Native endpoint

Through the native Microsoft 365 API, this operation is `GET /v1.0/me/mailFolders/:mailFolderId/childFolders` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-child-mail-folders.md) for the provider-specific parameters and requirements.

