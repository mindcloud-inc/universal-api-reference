# List Tags with Aspire

Retrieves takeoff items from your Aspire account.

## Endpoint

- **Method:** `GET`
- **Path:** `Tags`
- **Base URL:** `https://{environment}.youraspire.com/`
- **Official documentation:** [List Tags](https://cloud-api.youraspire.com/swagger/index.html)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `$expand` | query | `string` | no |
| `$filter` | query | `string` | no |
| `$orderby` | query | `string` | no |
| `$select` | query | `string` | no |
