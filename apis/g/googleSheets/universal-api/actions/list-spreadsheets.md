# Google Sheets: List Spreadsheets

Retrieves accessible Google Sheets files from Google Drive.

```
GET https://connect.mindcloud.co/v1/universal/googleSheets/latest/actions/list-spreadsheets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Sheets `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleSheets/latest/actions/list-spreadsheets?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleSheets/latest/actions/list-spreadsheets?${params}`, {
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
| `supportsAllDrives` | string | no | Default: `true`. |
| `includeItemsFromAllDrives` | string | no | Default: `true`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `q` | string | no | Default: `mimeType='application/vnd.google-apps.spreadsheet'`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdTime": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "modifiedTime": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdTime` | date | When the spreadsheet file was created in Google Drive. |
| `id` | string | Spreadsheet file ID. |
| `modifiedTime` | date | When the spreadsheet file was last modified in Google Drive. |
| `name` | string |  |

## Native endpoint

Through the native Google Sheets API, this operation is `GET https://www.googleapis.com/drive/v3/files` (base URL `https://sheets.googleapis.com/v4`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-spreadsheets.md) for the provider-specific parameters and requirements.

