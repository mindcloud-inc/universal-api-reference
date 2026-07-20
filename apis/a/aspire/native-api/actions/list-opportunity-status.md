# List Opportunity Status with Aspire

Retrieves opportunity statuses from your Aspire account.

## Endpoint

- **Method:** `GET`
- **Path:** `OpportunityStatuses`
- **Base URL:** `https://{environment}.youraspire.com/`
- **Official documentation:** [List Opportunity Status](https://guide.youraspire.com/apidocs/opportunity-status)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `$expand` | query | `string` | no |
| `$filter` | query | `string` | no |
| `$orderby` | query | `string` | no |
| `$select` | query | `string` | no |
