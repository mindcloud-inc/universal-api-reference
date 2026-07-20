# Microsoft 365 Excel: Delete Worksheet

Deletes a worksheet from a Microsoft 365 Excel workbook.

```
DELETE https://connect.mindcloud.co/v1/universal/microsoft365Excel/latest/actions/delete-worksheet
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft 365 Excel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/microsoft365Excel/latest/actions/delete-worksheet?connectionId=$CONNECTION_ID&driveItemId=string&worksheetName=RuntimeVerify" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "driveItemId": "string",
  "worksheetName": "RuntimeVerify"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoft365Excel/latest/actions/delete-worksheet?${params}`, {
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
| `driveItemId` | string | yes |  |
| `worksheetName` | string | yes | Example: `RuntimeVerify`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Microsoft 365 Excel API returns.

## Native endpoint

Through the native Microsoft 365 Excel API, this operation is `DELETE /v1.0/me/drive/items/{{driveItemId}}/workbook/worksheets('{{worksheetName}}')` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-worksheet.md) for the provider-specific parameters and requirements.

