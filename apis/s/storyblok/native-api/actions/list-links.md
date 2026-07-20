# List Links with Storyblok

Retrieves Storyblok links for the current space.

## Endpoint

- **Method:** `GET`
- **Path:** `/links`
- **Base URL:** `https://api.storyblok.com/v2/cdn`
- **Official documentation:** [List Links](https://www.storyblok.com/docs/api/content-delivery/v2/links/retrieve-multiple-links)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `version` | query | `string` | no | Whether to read draft or published content. |
