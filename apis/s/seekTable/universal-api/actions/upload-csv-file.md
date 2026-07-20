# SeekTable: Upload CSV File

Uploads a CSV file to a SeekTable cube.

```
POST https://connect.mindcloud.co/v1/universal/seekTable/latest/actions/upload-csv-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SeekTable `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/seekTable/latest/actions/upload-csv-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "Base64 CSV file contents or a file URL/path"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/seekTable/latest/actions/upload-csv-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "Base64 CSV file contents or a file URL/path"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file` | file | yes | CSV file content uploaded as multipart/form-data file. Example: `Base64 CSV file contents or a file URL/path`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cubeId` | string | no | GUID of an existing CSV cube to refresh. If not specified a new cube is created. Example: `50ae738e097c4ee89a66809588308d20`. |
| `filename` | string | no | Explicitly specified name of the CSV file. Useful when CSV content goes directly in the request body. Example: `sample.csv`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "CanAddReport": true,
      "CanDownloadDataFile": true,
      "CanEditSchema": true,
      "CanMoveReportUpstream": true,
      "CanSearch": true,
      "CanShareToTeam": true,
      "CreateDate": "2026-05-07T12:00:00.000Z",
      "Id": "string",
      "Name": "Ava Chen",
      "PivotFilterSuggestWithHint": true,
      "Shared": true,
      "SourceFile": "string",
      "SourceType": "string",
      "SourceTypeId": "string",
      "UpdateDate": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `CanAddReport` | boolean |  |
| `CanDownloadDataFile` | boolean |  |
| `CanEditSchema` | boolean |  |
| `CanMoveReportUpstream` | boolean |  |
| `CanSearch` | boolean |  |
| `CanShareToTeam` | boolean |  |
| `CreateDate` | date |  |
| `Id` | string | GUID of the created or refreshed cube. |
| `Name` | string | Cube name. |
| `PivotFilterSuggestWithHint` | boolean |  |
| `Shared` | boolean |  |
| `SourceFile` | string | Original CSV source file name. |
| `SourceType` | string | Human-readable source type label. |
| `SourceTypeId` | string | Machine-readable source type identifier. |
| `UpdateDate` | date |  |

## Native endpoint

Through the native SeekTable API, this operation is `POST /api/cube/import/csv` (base URL `https://www.seektable.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-csv-file.md) for the provider-specific parameters and requirements.

