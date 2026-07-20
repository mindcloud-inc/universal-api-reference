# Zoho Sheet: Get Content of Range

Retrieves the content of a range in Zoho Sheet.

```
GET https://connect.mindcloud.co/v1/universal/zohoSheet/latest/actions/get-content-of-range
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Sheet `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoSheet/latest/actions/get-content-of-range?connectionId=$CONNECTION_ID&resourceId=string&worksheetName=Ava%20Chen&startRow=1&startColumn=1&endRow=1&endColumn=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "resourceId": "string",
  "worksheetName": "Ava Chen",
  "startRow": "1",
  "startColumn": "1",
  "endRow": "1",
  "endColumn": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoSheet/latest/actions/get-content-of-range?${params}`, {
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
| `resourceId` | string | yes | The workbook resource ID. |
| `worksheetName` | string | yes | Name of the worksheet |
| `startRow` | number | yes | Start row index of the range |
| `startColumn` | number | yes | Start column index of the range |
| `endRow` | number | yes | End row index of the range |
| `endColumn` | number | yes | End column index of the range |

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
      "rangeDetails": [
        [
          {}
        ]
      ],
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
| `rangeDetails[]` | array<object> |  |
| `rangeDetails[].rowDetails[]` | array<object> |  |
| `rangeDetails[].rowDetails[].columnIndex` | number |  |
| `rangeDetails[].rowDetails[].content` | string |  |
| `rangeDetails[].rowIndex` | number |  |
| `status` | string |  |

## Native endpoint

Through the native Zoho Sheet API, this operation is `POST /:resourceId` (base URL `https://sheet.zoho.com/api/v2/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-content-of-range.md) for the provider-specific parameters and requirements.

