# List Stories in Folder with Storyblok

Retrieves stories from a specific Storyblok folder.

## Endpoint

- **Method:** `GET`
- **Path:** `/stories`
- **Base URL:** `https://api.storyblok.com/v2/cdn`
- **Official documentation:** [List Stories in Folder](https://www.storyblok.com/docs/api/content-delivery/v2/stories/examples/retrieving-stories-from-a-folder)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `starts_with` | query | `string` | yes | Only return stories whose full slug starts with this folder path prefix. |
| `version` | query | `string` | no | Whether to read draft or published content. |
