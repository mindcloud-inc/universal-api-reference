# Zoho Sheet: Delete Records from Worksheet

Deletes records from a worksheet in Zoho Sheet.

```
DELETE https://connect.mindcloud.co/v1/universal/zohoSheet/latest/actions/delete-records-from-worksheet
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Sheet `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/zohoSheet/latest/actions/delete-records-from-worksheet?connectionId=$CONNECTION_ID&resourceId=string&worksheetName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "resourceId": "string",
  "worksheetName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoSheet/latest/actions/delete-records-from-worksheet?${params}`, {
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
| `worksheetName` | string | yes | Name of the worksheet whose records needs to be deleted |
| `headerRow` | number | no | Optional parameter. By default, first row of the worksheet is considered as header row. This can be used if tabular data starts from any row other than the first row. |
| `criteria` | string | no | Mention the criteria as described above. |
| `rowArray` | string | no | Array of row indexes that need to be deleted. Provide this value as a valid JSON array string such as [4]. |
| `firstMatchOnly` | boolean | no | Optional parameter. If true and if there are multiple records on the specified criteria, records will be deleted for first match alone. Otherwise, all the matched records will be deleted. This parameter will be ignored if criteria is not mentioned. |
| `isCaseSensitive` | boolean | no | Optional parameter. By default it is true. Can be set as false for case insensitive search. |
| `deleteRows` | boolean | no | Optional parameter and by default it is false. If true it will delete the rows completely, otherwise the records are only erased by default. |

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
      "noOfRowsDeleted": 1,
      "noOfRowsRemaining": 1,
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
| `noOfRowsDeleted` | number |  |
| `noOfRowsRemaining` | number |  |
| `status` | string |  |

## Native endpoint

Through the native Zoho Sheet API, this operation is `POST /:resourceId` (base URL `https://sheet.zoho.com/api/v2/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-records-from-worksheet.md) for the provider-specific parameters and requirements.

