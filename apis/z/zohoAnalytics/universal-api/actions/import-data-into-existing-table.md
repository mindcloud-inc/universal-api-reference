# Zoho Analytics: Import Data Into Existing Table

Imports data into an existing Zoho Analytics table.

```
POST https://connect.mindcloud.co/v1/universal/zohoAnalytics/latest/actions/import-data-into-existing-table
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Analytics `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoAnalytics/latest/actions/import-data-into-existing-table" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "workspaceId": "string",
  "viewId": "string",
  "config": "[object Object]"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoAnalytics/latest/actions/import-data-into-existing-table', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "workspaceId": "string",
    "viewId": "string",
    "config": "[object Object]"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `workspaceId` | string | yes | ID of the workspace containing the target table. |
| `viewId` | string | yes | ID of the existing table view that should receive imported data. |
| `config` | string | yes | Required stringified JSON import configuration such as importType and fileType. Example: `[object Object]`. |
| `file` | file | no | Optional file payload to import. Provide either File or Data. |
| `data` | string | no | Optional raw CSV or JSON payload to import. Provide either Data or File. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {
        "columnDetails": {},
        "importErrors": "string",
        "importSummary": {
          "importOperation": "string",
          "importType": "string",
          "selectedColumnCount": 1,
          "successRowCount": 1,
          "totalColumnCount": 1,
          "totalRowCount": 1,
          "warnings": 1
        }
      },
      "status": "string",
      "summary": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.columnDetails` | object |  |
| `data.importErrors` | string |  |
| `data.importSummary.importOperation` | string |  |
| `data.importSummary.importType` | string |  |
| `data.importSummary.selectedColumnCount` | number |  |
| `data.importSummary.successRowCount` | number |  |
| `data.importSummary.totalColumnCount` | number |  |
| `data.importSummary.totalRowCount` | number |  |
| `data.importSummary.warnings` | number |  |
| `status` | string |  |
| `summary` | string |  |

## Native endpoint

Through the native Zoho Analytics API, this operation is `POST /workspaces/[:workspace-id]/views/[:view-id]/data` (base URL `https://analyticsapi.zoho.com/restapi/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/import-data-into-existing-table.md) for the provider-specific parameters and requirements.

