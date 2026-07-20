# List Company Officers with Société.com

Retrieves company officers from Société.com.

## Endpoint

- **Method:** `GET`
- **Path:** `/entreprise/:numid/dirigeants`
- **Base URL:** `https://api.societe.com/api/v1`
- **Official documentation:** [List Company Officers](https://api.societe.com/apisite/documentations/v1/documentation-api.html#societe-dirigeants-get)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `numid` | path | `string` | no | Company identifier or SIREN with officer data. |
