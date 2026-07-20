# Get Envelope Ids with eSign Genie

Retrieves envelope IDs from eSign Genie.

## Endpoint

- **Method:** `GET`
- **Path:** `/folders/getAllFolderIdsByStatus`
- **Base URL:** `https://na1.foxitesign.foxit.com/api`
- **Official documentation:** [Get Envelope Ids](https://docs.developer-api.foxit.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `dateFrom` | query | `date` | yes | Start date for the envelope search range. |
| `dateTo` | query | `date` | yes | End date for the envelope search range. |
| `status` | query | `string` | no | Optional Foxit eSign envelope status to filter by. |
