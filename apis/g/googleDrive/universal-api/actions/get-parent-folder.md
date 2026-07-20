# Google Drive: Get Parent Folder

Returns a Parent Folder for a File or Folder in Google Drive.

```
GET https://connect.mindcloud.co/v1/universal/googleDrive/latest/actions/get-parent-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Drive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleDrive/latest/actions/get-parent-folder?connectionId=$CONNECTION_ID&fileId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleDrive/latest/actions/get-parent-folder?${params}`, {
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
| `fields` | string | no | Projection fields to return from files.get. Use this action to retrieve parent metadata via the parents field. Default: `id,name,mimeType,parents`. |
| `fileId` | string | yes | The Id of a File to retrieve parent folders for. |

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

Through the native Google Drive API, this operation is `GET /drive/v3/files/:fileId` (base URL `https://www.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-parent-folder.md) for the provider-specific parameters and requirements.

