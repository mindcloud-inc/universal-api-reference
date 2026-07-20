# List Work Tickets with Aspire

Retrieves takeoff items from your Aspire account.

## Endpoint

- **Method:** `GET`
- **Path:** `WorkTickets`
- **Base URL:** `https://{environment}.youraspire.com/`
- **Official documentation:** [List Work Tickets](https://guide.youraspire.com/apidocs/worktickets-3)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `$filter` | query | `string` | no | Optional Aspire filter expression for narrowing work tickets. |
| `$orderby` | query | `string` | no | Optional Aspire sort expression for work ticket results. |
| `$select` | query | `string` | no | Optional comma-separated list of work ticket fields to return. |
| `$expand` | query | `string` | no | Optional Aspire expand expression for related work ticket data. |
