# List Company Financial Statements with Société.com

Retrieves company financial statements from Société.com.

## Endpoint

- **Method:** `GET`
- **Path:** `/entreprise/:numid/bilans`
- **Base URL:** `https://api.societe.com/api/v1`
- **Official documentation:** [List Company Financial Statements](https://api.societe.com/apisite/documentations/v1/documentation-api.html#societe-bilans-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `numid` | path | `string` | no | Company identifier or SIREN. |
