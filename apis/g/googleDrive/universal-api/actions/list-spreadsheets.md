# Google Drive: List Spreadsheets

Finds spreadsheets in Google Drive by query.

```
GET https://connect.mindcloud.co/v1/universal/googleDrive/latest/actions/list-spreadsheets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Drive `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleDrive/latest/actions/list-spreadsheets?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleDrive/latest/actions/list-spreadsheets?${params}`, {
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

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `orderBy` | string | no | Optional Google Drive orderBy expression, such as modifiedTime desc or name. Default: `modifiedTime desc`. Example: `modifiedTime desc`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdTime": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "modifiedTime": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "owners": [
        {
          "displayName": "Ava Chen",
          "emailAddress": "ava@example.com"
        }
      ],
      "shared": true,
      "webViewLink": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdTime` | date | Creation timestamp. |
| `id` | string | Google Drive file ID. |
| `modifiedTime` | date | Last modified timestamp. |
| `name` | string | Spreadsheet name. |
| `owners[].displayName` | string | Owner display name. |
| `owners[].emailAddress` | string | Owner email address. |
| `shared` | boolean | Whether the spreadsheet is shared. |
| `webViewLink` | string | Link to open the spreadsheet in Google Drive. |

## Native endpoint

Through the native Google Drive API, this operation is `GET /drive/v3/files` (base URL `https://www.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-spreadsheets.md) for the provider-specific parameters and requirements.

