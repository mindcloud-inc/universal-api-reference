# Zoho Sheet: Add Records to Worksheet

Adds records to a worksheet in Zoho Sheet.

```
POST https://connect.mindcloud.co/v1/universal/zohoSheet/latest/actions/add-records-to-worksheet
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Sheet `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoSheet/latest/actions/add-records-to-worksheet" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "resourceId": "string",
  "worksheetName": "Ava Chen",
  "jsonData": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoSheet/latest/actions/add-records-to-worksheet', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "resourceId": "string",
    "worksheetName": "Ava Chen",
    "jsonData": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `resourceId` | string | yes | The workbook resource ID. |
| `worksheetName` | string | yes | Name of the worksheet |
| `headerRow` | number | no | Optional parameter. Default value is 1. This can be mentioned if the table header is not in the first row of the worksheet. |
| `jsonData` | string | yes | JSON Array. Example : [{"Name":"Joe","Region":"South","Units":284},{"Name":"Beth","Region":"East","Units":290}]. "Name", "Region", and "Units" are the table headers. Provide this value as a valid JSON string. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `worksheetId` | string | no | Alternatively worksheet_id can be used instead of worksheet_name |

## Response

```json
{
  "success": true,
  "data": [
    {
      "endColumn": 1,
      "endRow": 1,
      "method": "string",
      "sheetName": "Ava Chen",
      "startColumn": 1,
      "startRow": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `endColumn` | number |  |
| `endRow` | number |  |
| `method` | string |  |
| `sheetName` | string |  |
| `startColumn` | number |  |
| `startRow` | number |  |
| `status` | string |  |

## Native endpoint

Through the native Zoho Sheet API, this operation is `POST /:resourceId` (base URL `https://sheet.zoho.com/api/v2/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-records-to-worksheet.md) for the provider-specific parameters and requirements.

