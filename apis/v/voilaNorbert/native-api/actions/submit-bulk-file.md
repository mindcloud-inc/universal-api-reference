# Submit Bulk File with VoilaNorbert

Submits a bulk email search file to VoilaNorbert.

## Endpoint

- **Method:** `POST`
- **Path:** `/massives/`
- **Base URL:** `https://api.voilanorbert.com/2018-01-08`
- **Official documentation:** [Submit Bulk File](https://api.voilanorbert.com/2018-01-08/#bulk-search-endpoint-bulk-operations-post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `col_company` | body | `string` | no | CSV column index containing the company name. |
| `col_name` | body | `string` | no | CSV column indexes containing first and last name values. |
| `content` | body | `string` | no | Raw CSV content to upload. |
