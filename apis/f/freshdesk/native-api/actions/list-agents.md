# List Agents with Freshdesk

Retrieves a list of agents from Freshdesk.

## Endpoint

- **Method:** `GET`
- **Path:** `/agents`
- **Base URL:** `https://{subdomain}.freshdesk.com/api/v2`
- **Official documentation:** [List Agents](https://developers.freshdesk.com/api/#list_all_agents)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [filtering](../README.md#filtering).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | no | — |
| `mobile` | query | `string` | no | — |
| `phone` | query | `string` | no | — |
| `state` | query | `list<string>` | no | Accepted values: `fulltime`, `occasional`. |
