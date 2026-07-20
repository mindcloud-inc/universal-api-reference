# Zoho Sheet: Fetch Records from Worksheet

Retrieves records from a worksheet in Zoho Sheet.

```
GET https://connect.mindcloud.co/v1/universal/zohoSheet/latest/actions/fetch-records-from-worksheet
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Sheet `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoSheet/latest/actions/fetch-records-from-worksheet?connectionId=$CONNECTION_ID&resourceId=string&worksheetName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "resourceId": "string",
  "worksheetName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoSheet/latest/actions/fetch-records-from-worksheet?${params}`, {
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
| `worksheetName` | string | yes | Name of the worksheet whose records needs to be fetched |
| `headerRow` | number | no | Optional parameter. By default, first row of the worksheet is considered as header row. This can be used if tabular data starts from any row other than the first row. |
| `criteria` | string | no | Optional parameter. Can be used to filter records. |
| `columnNames` | string | no | Optional parameter. Can be used to read particular column's data. By default all the column data will be available in response. Multiple column names must be separated by comma. |
| `renderOption` | string | no | Optional parameter. It defines how the value should be rendered. Possible options are formatted, unformatted, and formula. |
| `recordsStartIndex` | number | no | Optional parameter. This parameter can be used to get a few resources if there are too many. |
| `count` | number | no | Optional parameter. It denotes the number of records. |
| `isCaseSensitive` | boolean | no | Optional parameter. By default it is true. Can be set as false for case insensitive search. |

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
      "records": [
        [
          {}
        ]
      ],
      "recordsCount": 1,
      "recordsEndIndex": 1,
      "recordsStartIndex": 1,
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
| `records[]` | array<object> |  |
| `records[].name` | string |  |
| `records[].qty` | number |  |
| `records[].rowIndex` | number |  |
| `records[].status` | string |  |
| `recordsCount` | number |  |
| `recordsEndIndex` | number |  |
| `recordsStartIndex` | number |  |
| `status` | string |  |

## Native endpoint

Through the native Zoho Sheet API, this operation is `POST /:resourceId` (base URL `https://sheet.zoho.com/api/v2/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fetch-records-from-worksheet.md) for the provider-specific parameters and requirements.

