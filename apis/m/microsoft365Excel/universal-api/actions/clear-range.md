# Microsoft 365 Excel: Clear Range

Clears a worksheet range in Microsoft 365 Excel.

```
PUT https://connect.mindcloud.co/v1/universal/microsoft365Excel/latest/actions/clear-range
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft 365 Excel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/microsoft365Excel/latest/actions/clear-range" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "driveItemId": "string",
  "worksheetName": "RuntimeVerify",
  "startCell": "C1",
  "endCell": "C2"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoft365Excel/latest/actions/clear-range', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "driveItemId": "string",
    "worksheetName": "RuntimeVerify",
    "startCell": "C1",
    "endCell": "C2"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `driveItemId` | string | yes |  |
| `worksheetName` | string | yes | Example: `RuntimeVerify`. |
| `startCell` | string | yes | Example: `C1`. |
| `endCell` | string | yes | Example: `C2`. |
| `applyTo` | string | no | Default: `Contents`. Example: `Contents`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Microsoft 365 Excel API returns.

## Native endpoint

Through the native Microsoft 365 Excel API, this operation is `POST /v1.0/me/drive/items/{{driveItemId}}/workbook/worksheets('{{worksheetName}}')/range(address='{{startCell}}\:{{endCell}}')/clear` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/clear-range.md) for the provider-specific parameters and requirements.

