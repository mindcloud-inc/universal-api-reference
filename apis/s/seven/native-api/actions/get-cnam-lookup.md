# Get CNAM Lookup with Seven

Retrieves CNAM lookup details from Seven.

## Endpoint

- **Method:** `GET`
- **Path:** `/lookup/cnam`
- **Base URL:** `https://gateway.seven.io/api`
- **Official documentation:** [Get CNAM Lookup](https://docs.seven.io/en/rest-api/endpoints/lookup#cnam)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `number` | query | `string` | yes | The number to be queried. Multiple numbers must be separated by commas. You can enter almost any format; the API formats the number automatically. |
