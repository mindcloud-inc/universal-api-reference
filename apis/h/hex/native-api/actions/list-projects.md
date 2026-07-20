# List Projects with Hex

## Endpoint

- **Method:** `GET`
- **Path:** `/projects`
- **Base URL:** `https://app.hex.tech/api/v1`
- **Official documentation:** [List Projects](https://learn.hex.tech/docs/api-integrations/api/reference#operation/ListProjects)

## Capabilities

This operation supports [pagination](../README.md#pagination) and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `includeArchived` | query | `boolean` | no | Whether to include archived projects. |
| `includeComponents` | query | `boolean` | no | Whether to include components in the results. |
| `includeTrashed` | query | `boolean` | no | Whether to include trashed projects. |
| `includeSharing` | query | `boolean` | no | Whether to include sharing details in each project. |
| `statuses[]` | query | `array<string>` | no | Filter projects by status name. |
| `categories[]` | query | `array<string>` | no | Filter projects by category name. |
| `creatorEmail` | query | `string` | no | Filter projects by creator email. |
| `ownerEmail` | query | `string` | no | Filter projects by owner email. |
| `collectionId` | query | `string` | no | Filter projects by collection ID. |
