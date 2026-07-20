# Generate CSV File with EasyCSV

Creates a CSV file in EasyCSV from JSON data.

## Endpoint

- **Method:** `POST`
- **Path:** `/generate_csv/:generatorId`
- **Base URL:** `https://www.easycsv.io`

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `generatorId` | path | `string` | yes | The CSV Generator webhook token from the EasyCSV webhook URL. |
| `data` | query | `string` | yes | A JSON array of objects to turn into CSV rows. Send it as a stringified JSON array, matching the EasyCSV docs for the data parameter. |
| `recipient_email` | query | `string` | no | Optional email address to send the generated CSV file to. |
