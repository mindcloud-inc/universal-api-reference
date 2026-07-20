# Get Changelog with Productlane

Retrieves a changelog from your Productlane workspace.

## Endpoint

- **Method:** `GET`
- **Path:** `/changelogs/:workspaceId/:changelogId`
- **Base URL:** `https://productlane.com/api/v1`
- **Official documentation:** [Get Changelog](https://productlane.mintlify.dev/docs/api/changelogs/get-changelog)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `workspaceId` | path | `string` | yes |
| `changelogId` | path | `string` | yes |
| `language` | query | `string` | no |
