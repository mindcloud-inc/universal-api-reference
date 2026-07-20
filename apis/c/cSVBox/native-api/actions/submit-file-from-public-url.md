# Submit File From Public URL with CSVBox

## Endpoint

- **Method:** `POST`
- **Path:** `/file`
- **Base URL:** `https://api.csvbox.io/1.1`
- **Official documentation:** [Submit File From Public URL](https://help.csvbox.io/advanced-installation/rest-file-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `import.public_file_url` | body | `string` | yes | Publicly reachable URL for the CSV or spreadsheet file to import. |
| `import.sheet_license_key` | body | `string` | yes | CSVBox sheet license key that determines the destination sheet. |
| `import.file_sheet_name` | body | `string` | no | Worksheet name to import when the source file contains multiple tabs. |
| `import.auto_map` | body | `boolean` | no | Allow CSVBox to auto-map columns when exact matches are not found. |
| `import.user.user_id` | body | `string` | no | Optional user identifier to attach to the import metadata. |
| `import.options.has_header` | body | `boolean` | no | Whether the incoming file includes a header row. |
| `import.options.max_rows` | body | `number` | no | Optional maximum number of rows to import. |
