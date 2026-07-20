# List Company Establishments with Société.com

Retrieves company establishments from Société.com.

## Endpoint

- **Method:** `GET`
- **Path:** `/entreprise/:numid/etablissements`
- **Base URL:** `https://api.societe.com/api/v1`
- **Official documentation:** [List Company Establishments](https://api.societe.com/apisite/documentations/v1/documentation-api.html#societe-etablissements-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `numid` | path | `string` | no | Company identifier or SIREN. |
