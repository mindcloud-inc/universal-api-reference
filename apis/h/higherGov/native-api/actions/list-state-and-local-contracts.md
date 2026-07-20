# List State And Local Contracts with HigherGov

Retrieves state and local contract awards from HigherGov.

## Endpoint

- **Method:** `GET`
- **Path:** `/api-external/sl-contract/`
- **Base URL:** `https://www.highergov.com`
- **Official documentation:** [List State And Local Contracts](https://www.highergov.com/api-external/docs/#/api-external/api_external_sl_contract_list)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `captured_date` | query | `string` | no | Date the award was added to HigherGov |
| `end_date` | query | `string` | no | Latest end date for the award in YYYY-MM-DD format |
| `search_id` | query | `string` | no | HigherGov SearchID |
| `start_date` | query | `string` | no | Earliest start date for the award in YYYY-MM-DD format |
