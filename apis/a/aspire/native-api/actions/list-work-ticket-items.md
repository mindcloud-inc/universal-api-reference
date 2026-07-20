# List Work Ticket Items with Aspire

Retrieves work ticket items from your Aspire account.

## Endpoint

- **Method:** `GET`
- **Path:** `WorkTicketItems`
- **Base URL:** `https://{environment}.youraspire.com/`
- **Official documentation:** [List Work Ticket Items](https://guide.youraspire.com/apidocs/workticketitems-3)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `$expand` | query | `string` | no |
| `$filter` | query | `string` | no |
| `$orderby` | query | `string` | no |
| `$select` | query | `string` | no |
