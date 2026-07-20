# List Work Ticket Visits with Aspire

Retrieves work ticket visits from your Aspire account.

## Endpoint

- **Method:** `GET`
- **Path:** `WorkTicketVisits`
- **Base URL:** `https://{environment}.youraspire.com/`
- **Official documentation:** [List Work Ticket Visits](https://cloud-api.youraspire.com/swagger/index.html#/WorkTicketVisits/WorkTicketVisits_Get)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `$expand` | query | `string` | no |
| `$filter` | query | `string` | no |
| `$orderby` | query | `string` | no |
| `$select` | query | `string` | no |
