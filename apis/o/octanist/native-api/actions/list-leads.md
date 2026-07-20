# List Leads with Octanist

Retrieves leads from Octanist.

## Endpoint

- **Method:** `GET`
- **Path:** `/leads`
- **Base URL:** `https://octanist.com/api`
- **Official documentation:** [List Leads](https://octanist.com/docs/api-reference/endpoint/get-leads)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search` | query | `string` | no | Search across lead name, email, and phone. |
| `fields` | query | `string` | no | Comma-separated list of lead fields to return. |
