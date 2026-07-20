# List Customer Comments with actiTIME

Retrieves comments for a customer in actiTIME.

## Endpoint

- **Method:** `GET`
- **Path:** `/customers/:id/comments`
- **Base URL:** `{instanceUrl}/api/v1`
- **Official documentation:** [List Customer Comments](https://www.actitime.com/api-documentation/customers-resource)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Customer identifier. |
| `includeReferenced` | query | `string` | no | Comma-separated referenced objects to include. |
