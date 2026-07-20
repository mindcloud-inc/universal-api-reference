# Autocomplete Companies with OpenRegister

Finds company matches in OpenRegister as you type.

## Endpoint

- **Method:** `GET`
- **Path:** `/v1/autocomplete/company`
- **Base URL:** `https://api.openregister.de`
- **Official documentation:** [Autocomplete Companies](https://docs.openregister.de/endpoint/autocomplete-company)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | query | `string` | yes | Text search query to find companies by name. |
