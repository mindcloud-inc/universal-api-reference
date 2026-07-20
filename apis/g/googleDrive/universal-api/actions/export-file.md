# Google Drive: Export File

Exports a Google Workspace document from Google Drive.

```
GET https://connect.mindcloud.co/v1/universal/googleDrive/latest/actions/export-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Drive `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleDrive/latest/actions/export-file?connectionId=$CONNECTION_ID&fileId=string&mimeType=application%2Fpdf" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fileId": "string",
  "mimeType": "application/pdf"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleDrive/latest/actions/export-file?${params}`, {
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
| `fileId` | list | yes | Select a Google Workspace file to export. With drive.file access, Google only allows files created by or explicitly authorized to the app. |
| `mimeType` | list | yes | The export format to request from Google Drive files.export. One of: `application/pdf`, `application/rtf`, `application/vnd.oasis.opendocument.text`, `application/vnd.openxmlformats-officedocument.presentationml.presentation`, `application/vnd.openxmlformats-officedocument.spreadsheetml.sheet`, `application/vnd.openxmlformats-officedocument.wordprocessingml.document`, `text/plain`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Google Drive API returns.

## Native endpoint

Through the native Google Drive API, this operation is `GET /drive/v3/files/:fileId/export` (base URL `https://www.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/export-file.md) for the provider-specific parameters and requirements.

