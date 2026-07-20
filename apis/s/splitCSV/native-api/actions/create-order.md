# Create Order with Split CSV

Creates a new file-processing order in Split CSV.

## Endpoint

- **Method:** `POST`
- **Path:** `/app/api/v1/orders`
- **Base URL:** `https://www.splitcsv.com`
- **Official documentation:** [Create Order](https://www.splitcsv.com/developers/core/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `string` | yes | The HTTPS URL of the source file to split. |
| `method` | body | `list` | yes | The split method to apply to the source file. Accepted values: `filecount`, `filesize`, `headervalue`, `linecount`, `linesperfile`, `passthrough`, `sqlite3`. |
| `filecount` | body | `number` | no | The number of files to produce. Required when method is filecount. |
| `filesize` | body | `number` | no | The target size in bytes for each split file. Required when method is filesize. |
| `linecount` | body | `number` | no | The number of lines to include in each file. Required when method is linecount. |
| `linesperfile` | body | `number` | no | The number of records to include in each file. Required when method is linesperfile. |
| `targetheader` | body | `number` | no | The zero-based column index whose header value should be used for splitting. Required when method is headervalue. |
| `headers` | body | `number` | no | The number of header lines to replicate into each output file. |
| `skip` | body | `number` | no | The number of leading lines to skip before parsing the source file. |
| `xlsx` | body | `boolean` | no | When true, save the output files in Excel XLSX format. |
| `json` | body | `boolean` | no | When true, save the output files as newline-delimited JSON. |
| `tabname` | body | `string` | no | The worksheet name to use when xlsx is true. |
| `detectduplicates` | body | `boolean` | no | When true, duplicate rows are written to a separate duplicates.csv file and remain in the split output. |
| `removeduplicates` | body | `boolean` | no | When true, duplicate rows are written to a separate duplicates.csv file and removed from the split output. |
| `usequotes` | body | `boolean` | no | When false, output CSV fields are not quoted. |
| `delimiter` | body | `string` | no | The delimiter character to use when parsing the source file instead of a comma. |
| `outputdelimiter` | body | `string` | no | The delimiter character to use when generating the split output files instead of a comma. |
| `drop[]` | body | `array<number>` | no | The zero-based column indexes to remove from the output. |
| `notification_url` | body | `string` | no | The HTTPS webhook URL to notify when the split completes. |
| `per_file` | body | `boolean` | no | When true, send a separate webhook for each output file after completion. |
