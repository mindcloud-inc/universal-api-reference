# List Links in Folder with Storyblok

Retrieves Storyblok links from a specific folder.

## Endpoint

- **Method:** `GET`
- **Path:** `/links`
- **Base URL:** `https://api.storyblok.com/v2/cdn`
- **Official documentation:** [List Links in Folder](https://www.storyblok.com/docs/api/content-delivery/v2/links/retrieve-multiple-links)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `starts_with` | query | `string` | yes | Only return links whose real path starts with this folder path prefix. |
| `version` | query | `string` | no | Whether to read draft or published content. |
