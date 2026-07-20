# List Property Status with Aspire

Retrieves property statuses from your Aspire account.

## Endpoint

- **Method:** `GET`
- **Path:** `PropertyStatuses`
- **Base URL:** `https://{environment}.youraspire.com/`
- **Official documentation:** [List Property Status](https://guide.youraspire.com/apidocs/propertytypes-3)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `$expand` | query | `string` | no |
| `$filter` | query | `string` | no |
| `$orderby` | query | `string` | no |
| `$select` | query | `string` | no |
