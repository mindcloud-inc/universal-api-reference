# Search Deals with Teamgate

Finds deals in Teamgate.

## Endpoint

- **Method:** `GET`
- **Path:** `/deals`
- **Base URL:** `https://api.teamgate.com/v4`
- **Official documentation:** [Search Deals](https://developers.teamgate.com/#bc81c42a-8448-43af-8991-4eeea7feeef1)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name[like]` | query | `string` | yes | Substring match for the deal name. Use Teamgate % wildcards when needed, for example %Codex%. |
| `source` | query | `string` | no | Deal source name filter. |
| `operator` | query | `string` | no | Logical operator for combining search conditions, such as OR. |
| `fields` | query | `string` | no | Comma-separated fields to return in the search response. |
