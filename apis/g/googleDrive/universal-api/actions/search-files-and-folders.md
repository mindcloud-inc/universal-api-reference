# Google Drive: Search Files and Folders

Search Files & Folders in Google Drive.

```
GET https://connect.mindcloud.co/v1/universal/googleDrive/latest/actions/search-files-and-folders
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Drive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleDrive/latest/actions/search-files-and-folders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleDrive/latest/actions/search-files-and-folders?${params}`, {
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
| `parents` | list<string> | no | Optionally, select a specific folder to search for files in. |
| `mimeType` | list<string> | no | Restrict the search to specific file types. If you want all file types, leave this field blank. Default: `application/vnd.google-apps.file`. |
| `searchType` | list<string> | no | Searching with 'Name' requires a Search Type. File Name Contains or File Name is Exactly. Use contains when looking for more than 1 file. Example, File Name Contains: 'PO# ' Default: `CONTAINS`. |
| `q` | string | no | Enter a File/Folder Name or type a phrase to search in file content. Example, "TEMPLATES". Then enter a "Search Type". |
| `fields` | string | no | Default: `*`. |
| `orderBy` | string | no | name,recency,etc. Default: `recency`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "kind": "string",
      "mimeType": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `kind` | string |  |
| `mimeType` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Google Drive API, this operation is `GET /drive/v3/files` (base URL `https://www.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-files-and-folders.md) for the provider-specific parameters and requirements.

