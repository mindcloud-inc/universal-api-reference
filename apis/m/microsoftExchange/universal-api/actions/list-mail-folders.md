# Microsoft Exchange: List Mail Folders

Retrieves mail folders from Microsoft Exchange.

```
GET https://connect.mindcloud.co/v1/universal/microsoftExchange/latest/actions/list-mail-folders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Exchange `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoftExchange/latest/actions/list-mail-folders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoftExchange/latest/actions/list-mail-folders?${params}`, {
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
| `top` | number | no | Upper bound on the number of top-level folders to return from the current page. Default: `25`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `includeHiddenFolders` | boolean | no | Whether to include hidden mail folders in the results. |

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
| `displayName` | string | The mail folder display name. |
| `id` | string | The mail folder ID. |
| `isHidden` | boolean | Whether the folder is hidden. |
| `parentFolderId` | string | The parent mail folder ID. |
| `totalItemCount` | number | The total number of items. |
| `unreadItemCount` | number | The number of unread items. |

## Native endpoint

Through the native Microsoft Exchange API, this operation is `GET /v1.0/me/mailFolders` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-mail-folders.md) for the provider-specific parameters and requirements.

