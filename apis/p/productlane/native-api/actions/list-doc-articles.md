# List Doc Articles with Productlane

Retrieves help center articles from Productlane.

## Endpoint

- **Method:** `GET`
- **Path:** `/docs/articles/{workspaceId}`
- **Base URL:** `https://productlane.com/api/v1`
- **Official documentation:** [List Doc Articles](https://productlane.mintlify.dev/docs/api/docs/list-doc-articles)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `string` | yes | Workspace ID to list published doc articles for. |
| `language` | query | `string` | no | Optional language filter. |
| `groupId` | query | `string` | no | Optional docs group filter. |
