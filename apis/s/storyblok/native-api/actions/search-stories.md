# Search Stories with Storyblok

Finds Storyblok stories by search term.

## Endpoint

- **Method:** `GET`
- **Path:** `/stories`
- **Base URL:** `https://api.storyblok.com/v2/cdn`
- **Official documentation:** [Search Stories](https://www.storyblok.com/docs/api/content-delivery/v2/stories/retrieve-multiple-stories)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `search_term` | query | `string` | yes | The free-text search term to use when listing stories. |
