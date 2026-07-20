# Upload lead file with LeadTable

## Endpoint

- **Method:** `POST`
- **Path:** `/addFile`
- **Base URL:** `https://api.lead-table.com/api/v3/external`
- **Official documentation:** [Upload lead file](https://docs.lead-table.com/leadtable-external-api-v3)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `file` | body | `file` | yes | The file to upload to the lead. |
| `id` | body | `string` | yes | The lead that should receive the file. |
