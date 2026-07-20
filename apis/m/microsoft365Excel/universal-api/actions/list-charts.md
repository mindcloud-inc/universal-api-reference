# Microsoft 365 Excel: List Charts

Retrieves charts from a worksheet in Microsoft 365 Excel.

```
GET https://connect.mindcloud.co/v1/universal/microsoft365Excel/latest/actions/list-charts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft 365 Excel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoft365Excel/latest/actions/list-charts?connectionId=$CONNECTION_ID&driveItemId=string&worksheetName=RuntimeVerify" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "driveItemId": "string",
  "worksheetName": "RuntimeVerify"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoft365Excel/latest/actions/list-charts?${params}`, {
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

```json
{
  "success": true,
  "data": [
    {
      "chartType": "string",
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `chartType` | string |  |
| `id` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Microsoft 365 Excel API, this operation is `GET /v1.0/me/drive/items/{{driveItemId}}/workbook/worksheets('{{worksheetName}}')/charts` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-charts.md) for the provider-specific parameters and requirements.

