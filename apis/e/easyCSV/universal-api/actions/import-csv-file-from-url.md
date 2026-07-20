# EasyCSV: Import CSV File From URL

Imports a CSV file into EasyCSV from a public URL.

```
POST https://connect.mindcloud.co/v1/universal/easyCSV/latest/actions/import-csv-file-from-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EasyCSV `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/easyCSV/latest/actions/import-csv-file-from-url" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceSlug": "string",
  "webhookId": "string",
  "publicFileUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/easyCSV/latest/actions/import-csv-file-from-url', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceSlug": "string",
    "webhookId": "string",
    "publicFileUrl": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspaceSlug` | string | yes | The first path segment after easycsv.io in the sheet webhook URL, for example mindcloudco. |
| `webhookId` | string | yes | The final UUID segment in the sheet webhook URL. |
| `publicFileUrl` | string | yes | A public URL pointing to the CSV or XLSX file to import. |
| `importerEmail` | string | no | Optional email address to notify when the import finishes. |
| `importName` | string | no | Optional name to label this import run in EasyCSV. |
| `importCode` | string | no | Optional import code to group or identify this import. |
| `extraColumns` | string | no | Optional JSON object string of extra columns to add to every imported row. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "import_code": "string",
      "import_id": "string",
      "message": "string",
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `import_code` | string | Import code echoed back by EasyCSV when provided. |
| `import_id` | string | EasyCSV import identifier for the queued job. |
| `message` | string | Provider message describing the import result. |
| `status` | number | HTTP-style status returned by EasyCSV for the queued import. |

## Native endpoint

Through the native EasyCSV API, this operation is `POST https://www.easycsv.io/:workspaceSlug/sheets/webhook/:webhookId` (base URL `https://www.easycsv.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/import-csv-file-from-url.md) for the provider-specific parameters and requirements.

