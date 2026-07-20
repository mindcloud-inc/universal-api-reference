# Microsoft 365 Excel: Update Worksheet

Updates a worksheet in a Microsoft 365 Excel workbook.

```
PUT https://connect.mindcloud.co/v1/universal/microsoft365Excel/latest/actions/update-worksheet
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft 365 Excel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/microsoft365Excel/latest/actions/update-worksheet" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "driveItemId": "string",
  "worksheetName": "RuntimeVerify"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoft365Excel/latest/actions/update-worksheet', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "driveItemId": "string",
    "worksheetName": "RuntimeVerify"
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
| `name` | string | no | Example: `RuntimeVerifyRenamed`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `visibility` | string | no | Example: `Visible`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "name": "Ava Chen",
      "position": 1,
      "visibility": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `name` | string |  |
| `position` | number |  |
| `visibility` | string |  |

## Native endpoint

Through the native Microsoft 365 Excel API, this operation is `PATCH /v1.0/me/drive/items/{{driveItemId}}/workbook/worksheets('{{worksheetName}}')` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-worksheet.md) for the provider-specific parameters and requirements.

