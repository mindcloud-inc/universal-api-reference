# Ragic: Update Record

Updates an existing record in Ragic.

```
PUT https://connect.mindcloud.co/v1/universal/ragic/latest/actions/update-record
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ragic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/ragic/latest/actions/update-record" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "tabFolderPath": "ragic-setup",
  "sheetIndex": "8",
  "recordId": "0"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ragic/latest/actions/update-record', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "tabFolderPath": "ragic-setup",
    "sheetIndex": "8",
    "recordId": "0"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tabFolderPath` | string | yes | The folder path from the Ragic URL, for example `ragic-setup`. Default: `ragic-setup`. |
| `sheetIndex` | number | yes | The sheet number from the Ragic URL. Default: `8`. |
| `recordId` | number | yes | The record ID from the Ragic record URL. Default: `0`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `doFormula` | boolean | no | Recalculate formulas before saving. |
| `doDefaultValue` | boolean | no | Load default values when updating the record. |
| `doLinkLoad` | string | no | Run Ragic link-and-load logic. Use `true` or `first`. |
| `doWorkflow` | boolean | no | Execute the workflow script associated with this update. |
| `notification` | boolean | no | Send notifications to relevant users. |
| `checkLock` | boolean | no | Check whether the record is locked before updating. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Ragic API returns.

## Native endpoint

Through the native Ragic API, this operation is `POST /:tabFolderPath/:sheetIndex/:recordId` (base URL `{{credentials.serverUrl}}/mindcloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-record.md) for the provider-specific parameters and requirements.

