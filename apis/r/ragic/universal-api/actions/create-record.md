# Ragic: Create Record

Creates a new record in Ragic.

```
POST https://connect.mindcloud.co/v1/universal/ragic/latest/actions/create-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ragic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ragic/latest/actions/create-record" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tabFolderPath": "ragic-setup",
  "sheetIndex": "8"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ragic/latest/actions/create-record', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tabFolderPath": "ragic-setup",
    "sheetIndex": "8"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tabFolderPath` | string | yes | Folder path segment before the sheet index in the Ragic URL, for example ragic-setup. Default: `ragic-setup`. |
| `sheetIndex` | number | yes | Numeric sheet identifier from the target Ragic resource URL. Default: `8`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `doFormula` | boolean | no | Recalculate formulas before create. When true, workflow scripts will not run. |
| `doDefaultValue` | boolean | no | Load default values when creating the record. |
| `doLinkLoad` | string | no | Execute link/load operations. Use true to run after formulas or first to run before formulas. |
| `doWorkflow` | boolean | no | Execute the workflow script associated with the sheet. |
| `notification` | boolean | no | Send notifications to relevant users. Ragic defaults this to true when omitted. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Ragic API returns.

## Native endpoint

Through the native Ragic API, this operation is `POST /:tabFolderPath/:sheetIndex` (base URL `{{credentials.serverUrl}}/mindcloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-record.md) for the provider-specific parameters and requirements.

