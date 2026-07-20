# List Companies with Aspire

Retrieves a list of commercial or enterprise businesses associated with a contact.

## Endpoint

- **Method:** `GET`
- **Path:** `Companies`
- **Base URL:** `https://{environment}.youraspire.com/`
- **Official documentation:** [List Companies](https://guide.youraspire.com/apidocs/companies-6)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `$expand` | query | `string` | no |
| `$filter` | query | `string` | no |
| `$orderby` | query | `string` | no |
| `$select` | query | `string` | no |
