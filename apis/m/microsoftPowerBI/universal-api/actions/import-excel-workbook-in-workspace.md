# Microsoft Power BI: Import Excel Workbook in Workspace



```
POST https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/import-excel-workbook-in-workspace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Power BI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/import-excel-workbook-in-workspace" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "groupId": "d5a55202-2ad7-487c-8c05-85a7092b4924",
  "filePath": "/Documents/MindCloud MC-21089.xlsx"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoftPowerBI/latest/actions/import-excel-workbook-in-workspace', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "groupId": "d5a55202-2ad7-487c-8c05-85a7092b4924",
    "filePath": "/Documents/MindCloud MC-21089.xlsx"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `groupId` | string | yes | Power BI workspace ID that will receive the imported Excel workbook. Example: `d5a55202-2ad7-487c-8c05-85a7092b4924`. |
| `filePath` | string | yes | OneDrive for Business path to the Excel .xlsx workbook to import. Example: `/Documents/MindCloud MC-21089.xlsx`. |
| `connectionType` | list | no | Optional. Power BI import connection type for a OneDrive for Business Excel file. One of: `0`, `1`. |
| `nameConflict` | list | no | Optional. Conflict handling mode for an import with the same name. Power BI defaults to Ignore. One of: `0`, `1`, `2`, `3`, `4`. Default: `Ignore`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdDateTime": "2026-05-07T12:00:00.000Z",
      "datasets": [
        {}
      ],
      "error": {},
      "id": "string",
      "importState": "string",
      "name": "Ava Chen",
      "reports": [
        {}
      ],
      "updatedDateTime": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdDateTime` | date | Import creation time. |
| `datasets` | array<object> | Datasets associated with this import. |
| `error` | object | Error details when the import fails. |
| `id` | string | Power BI import ID. |
| `importState` | string | Import state such as Publishing, Succeeded, or Failed. |
| `name` | string | Import name. |
| `reports` | array<object> | Reports associated with this import. |
| `updatedDateTime` | date | Import last update time. |

## Native endpoint

Through the native Microsoft Power BI API, this operation is `POST groups/[:groupId]/imports` (base URL `https://api.powerbi.com/v1.0/myorg`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/import-excel-workbook-in-workspace.md) for the provider-specific parameters and requirements.

