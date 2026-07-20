# Zoho Sheet: Set Content to Range

Updates the content of a range in Zoho Sheet.

```
PUT https://connect.mindcloud.co/v1/universal/zohoSheet/latest/actions/set-content-to-range
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Sheet `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zohoSheet/latest/actions/set-content-to-range" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "resourceId": "string",
  "worksheetName": "Ava Chen",
  "row": 1,
  "column": 1,
  "data": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoSheet/latest/actions/set-content-to-range', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "resourceId": "string",
    "worksheetName": "Ava Chen",
    "row": 1,
    "column": 1,
    "data": "string"
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
| `row` | number | yes | Row index of the cell from which CSV data will start |
| `column` | number | yes | Column index of the cell from which CSV data will start |
| `ignoreEmpty` | boolean | no | If set to true empty value in CSV data will be ignored |
| `data` | string | yes | CSV data |

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
      "method": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `method` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Zoho Sheet API, this operation is `POST /:resourceId` (base URL `https://sheet.zoho.com/api/v2/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-content-to-range.md) for the provider-specific parameters and requirements.

