# List Changelogs with Productlane

Retrieves changelogs from your Productlane workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/changelogs/:workspaceId`
- **Base URL:** `https://productlane.com/api/v1`
- **Official documentation:** [List Changelogs](https://productlane.mintlify.dev/docs/api/changelogs/list-changelogs)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `string` | yes |
| `language` | query | `string` | no |
