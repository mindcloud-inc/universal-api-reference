# List Property Availabilities with Aspire

Retrieves property availability records from your Aspire account.

## Endpoint

- **Method:** `GET`
- **Path:** `PropertyAvailabilities`
- **Base URL:** `https://{environment}.youraspire.com/`
- **Official documentation:** [List Property Availabilities](https://cloud-api.youraspire.com/swagger/index.html#/PropertyAvailabilities/PropertyAvailabilities_Get)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `$expand` | query | `string` | no |
| `$filter` | query | `string` | no |
| `$orderby` | query | `string` | no |
| `$select` | query | `string` | no |
