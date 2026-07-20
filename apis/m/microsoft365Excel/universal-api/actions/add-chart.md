# Microsoft 365 Excel: Add Chart

Creates a chart in a Microsoft 365 Excel worksheet.

```
POST https://connect.mindcloud.co/v1/universal/microsoft365Excel/latest/actions/add-chart
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft 365 Excel `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/microsoft365Excel/latest/actions/add-chart" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "driveItemId": "string",
  "worksheetName": "RuntimeVerify",
  "type": "ColumnClustered",
  "sourceData": "A1:B3"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoft365Excel/latest/actions/add-chart', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "driveItemId": "string",
    "worksheetName": "RuntimeVerify",
    "type": "ColumnClustered",
    "sourceData": "A1:B3"
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
| `type` | string | yes | Default: `ColumnClustered`. Example: `ColumnClustered`. |
| `sourceData` | string | yes | Range address for the chart source data, for example A1:B3. Example: `A1:B3`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `seriesBy` | string | no | Default: `Auto`. Example: `Auto`. |

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

Through the native Microsoft 365 Excel API, this operation is `POST /v1.0/me/drive/items/{{driveItemId}}/workbook/worksheets('{{worksheetName}}')/charts/add` (base URL `https://graph.microsoft.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-chart.md) for the provider-specific parameters and requirements.

