# List Docs with Coda

Retrieves accessible docs from Coda workspaces.

## Endpoint

- **Method:** `GET`
- **Path:** `/docs`
- **Base URL:** `https://coda.io/apis/v1`
- **Official documentation:** [List Docs](https://coda.io/developers/apis/v1#tag/Docs/operation/listDocs)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `isOwner` | query | `boolean` | no | Show only docs owned by the user. |
| `isPublished` | query | `boolean` | no | Show only published docs. |
| `query` | query | `string` | no | Search term used to filter docs. |
| `sourceDoc` | query | `string` | no | Show only docs copied from this doc ID. |
| `isStarred` | query | `boolean` | no | If true returns starred docs, if false returns unstarred docs. |
| `inGallery` | query | `boolean` | no | Show only docs visible within the gallery. |
| `workspaceId` | query | `string` | no | Show only docs belonging to this workspace ID. |
| `folderId` | query | `string` | no | Show only docs belonging to this folder ID. |
