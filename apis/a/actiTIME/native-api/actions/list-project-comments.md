# List Project Comments with actiTIME

Retrieves comments for a project in actiTIME.

## Endpoint

- **Method:** `GET`
- **Path:** `/projects/:id/comments`
- **Base URL:** `{instanceUrl}/api/v1`
- **Official documentation:** [List Project Comments](https://www.actitime.com/api-documentation/projects-resource)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Project identifier. |
| `includeReferenced` | query | `string` | no | Comma-separated referenced objects to include. |
