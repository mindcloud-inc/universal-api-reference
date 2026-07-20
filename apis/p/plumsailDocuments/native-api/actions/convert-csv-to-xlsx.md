# Convert CSV to XLSX with Plumsail Documents

Converts CSV to XLSX in Plumsail Documents.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/convert/csv-to-xlsx`
- **Base URL:** `https://us-api.plumsail.com`
- **Official documentation:** [Convert CSV to XLSX](https://us-api.plumsail.com/swagger/index.html?urls.primaryName=Documents%20V2%20(US)#/Convert)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `HasHeaderRecords` | body | `boolean` | no | Whether the CSV includes a header row. |
| `Delimiter` | body | `string` | no | Delimiter character used in the CSV file. |
| `Locale` | body | `string` | no | Locale used when parsing CSV values. |
| `Limit` | body | `number` | no | Maximum number of CSV rows to convert. |
| `Mappings` | body | `string` | no | JSON mapping rules for CSV columns and output fields. |
| `File` | body | `file` | no | CSV file to upload. |
| `FileUrl` | body | `string` | no | Anonymous URL to a CSV file. |
| `CallbackUrl` | body | `string` | no | Webhook URL to receive async completion notifications. |
