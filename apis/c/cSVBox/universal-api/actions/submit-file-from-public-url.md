# CSVBox: Submit File From Public URL



```
POST https://connect.mindcloud.co/v1/universal/cSVBox/latest/actions/submit-file-from-public-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CSVBox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/cSVBox/latest/actions/submit-file-from-public-url" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "publicFileUrl": "https://example.com",
  "sheetLicenseKey": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cSVBox/latest/actions/submit-file-from-public-url', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "publicFileUrl": "https://example.com",
    "sheetLicenseKey": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `publicFileUrl` | string | yes | Publicly reachable URL for the CSV or spreadsheet file to import. |
| `sheetLicenseKey` | string | yes | CSVBox sheet license key that determines the destination sheet. |
| `hasHeader` | boolean | no | Whether the incoming file includes a header row. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fileSheetName` | string | no | Worksheet name to import when the source file contains multiple tabs. |
| `autoMap` | boolean | no | Allow CSVBox to auto-map columns when exact matches are not found. |
| `userId` | string | no | Optional user identifier to attach to the import metadata. |
| `maxRows` | number | no | Optional maximum number of rows to import. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "custom_fields": {},
      "destination_type": "string",
      "dynamic_columns": {},
      "env_name": "Ava Chen",
      "import_id": 1,
      "import_starttime": 1,
      "options": {},
      "sheet_id": 1,
      "sheet_name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `custom_fields` | object | User-linked custom fields returned by CSVBox. |
| `destination_type` | string | Configured destination type for the import. |
| `dynamic_columns` | object | Dynamic column payload returned by CSVBox. |
| `env_name` | string | CSVBox environment name for the import. |
| `import_id` | number | CSVBox import identifier. |
| `import_starttime` | number | Import start timestamp returned by CSVBox. |
| `options` | object | Applied import options returned by CSVBox. |
| `sheet_id` | number | Numeric CSVBox sheet identifier. |
| `sheet_name` | string | CSVBox sheet name. |

## Native endpoint

Through the native CSVBox API, this operation is `POST /file` (base URL `https://api.csvbox.io/1.1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/submit-file-from-public-url.md) for the provider-specific parameters and requirements.

