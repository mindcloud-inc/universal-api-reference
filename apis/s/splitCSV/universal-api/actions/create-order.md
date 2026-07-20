# Split CSV: Create Order

Creates a new file-processing order in Split CSV.

```
POST https://connect.mindcloud.co/v1/universal/splitCSV/latest/actions/create-order
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Split CSV `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/splitCSV/latest/actions/create-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "https://raw.githubusercontent.com/cs109/2014_data/master/countries.csv",
  "method": "filecount"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/splitCSV/latest/actions/create-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "https://raw.githubusercontent.com/cs109/2014_data/master/countries.csv",
    "method": "filecount"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file` | string | yes | The HTTPS URL of the source file to split. Example: `https://raw.githubusercontent.com/cs109/2014_data/master/countries.csv`. |
| `method` | list | yes | The split method to apply to the source file. One of: `filecount`, `filesize`, `headervalue`, `linecount`, `linesperfile`, `passthrough`, `sqlite3`. Example: `filecount`. |
| `fileCount` | number | no | The number of files to produce. Required when method is filecount. Example: `2`. |
| `fileSize` | number | no | The target size in bytes for each split file. Required when method is filesize. Example: `1048576`. |
| `lineCount` | number | no | The number of lines to include in each file. Required when method is linecount. Example: `1000`. |
| `linesPerFile` | number | no | The number of records to include in each file. Required when method is linesperfile. Example: `500`. |
| `targetHeader` | number | no | The zero-based column index whose header value should be used for splitting. Required when method is headervalue. Example: `0`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `headers` | number | no | The number of header lines to replicate into each output file. Example: `1`. |
| `skip` | number | no | The number of leading lines to skip before parsing the source file. Example: `0`. |
| `xlsx` | boolean | no | When true, save the output files in Excel XLSX format. Example: `false`. |
| `json` | boolean | no | When true, save the output files as newline-delimited JSON. Example: `false`. |
| `tabName` | string | no | The worksheet name to use when xlsx is true. Example: `Split CSV Output`. |
| `detectDuplicates` | boolean | no | When true, duplicate rows are written to a separate duplicates.csv file and remain in the split output. Example: `false`. |
| `removeDuplicates` | boolean | no | When true, duplicate rows are written to a separate duplicates.csv file and removed from the split output. Example: `false`. |
| `useQuotes` | boolean | no | When false, output CSV fields are not quoted. Example: `true`. |
| `delimiter` | string | no | The delimiter character to use when parsing the source file instead of a comma. Example: `,`. |
| `outputDelimiter` | string | no | The delimiter character to use when generating the split output files instead of a comma. Example: `;`. |
| `drop[]` | array<number> | no | The zero-based column indexes to remove from the output. Example: `0,2`. |
| `notificationUrl` | string | no | The HTTPS webhook URL to notify when the split completes. Example: `https://example.com/splitcsv-webhook`. |
| `perFile` | boolean | no | When true, send a separate webhook for each output file after completion. Example: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "order": {
        "created": "2026-05-07T12:00:00.000Z",
        "id": "string",
        "name": "Ava Chen"
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | The created order id. |
| `order` | object | The created order object. |
| `order.created` | date | The order creation timestamp in ISO8601 format. |
| `order.id` | string | The order id. |
| `order.name` | string | The order name, typically driven by the source file name. |
| `success` | boolean | Whether the order was created successfully. |

## Native endpoint

Through the native Split CSV API, this operation is `POST /app/api/v1/orders` (base URL `https://www.splitcsv.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-order.md) for the provider-specific parameters and requirements.

