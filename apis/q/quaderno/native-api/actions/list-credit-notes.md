# List Credit Notes with Quaderno

Retrieves credit notes from Quaderno.

## Endpoint

- **Method:** `GET`
- **Path:** `/credits`
- **Base URL:** `https://sandbox-quadernoapp.com/api`
- **Official documentation:** [List Credit Notes](https://developers.quaderno.io/api/#tag/Credits/operation/listCredits)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `q` | query | `string` | no | Search text to filter credit notes. |
| `date` | query | `date` | no | Date filter for credit notes. |
| `state` | query | `string` | no | State selector for credit notes. |
| `processor_id` | query | `string` | no | Payment processor ID selector for credit notes. |
