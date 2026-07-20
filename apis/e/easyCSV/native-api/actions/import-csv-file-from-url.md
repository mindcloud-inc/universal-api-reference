# Import CSV File From URL with EasyCSV

Imports a CSV file into EasyCSV from a public URL.

## Endpoint

- **Method:** `POST`
- **Path:** `https://www.easycsv.io/:workspaceSlug/sheets/webhook/:webhookId`
- **Base URL:** `https://www.easycsv.io`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceSlug` | path | `string` | yes | The first path segment after easycsv.io in the sheet webhook URL, for example mindcloudco. |
| `webhookId` | path | `string` | yes | The final UUID segment in the sheet webhook URL. |
| `public_file_url` | query | `string` | yes | A public URL pointing to the CSV or XLSX file to import. |
| `importer_email` | query | `string` | no | Optional email address to notify when the import finishes. |
| `import_name` | query | `string` | no | Optional name to label this import run in EasyCSV. |
| `import_code` | query | `string` | no | Optional import code to group or identify this import. |
| `extra_columns` | query | `string` | no | Optional JSON object string of extra columns to add to every imported row. |
