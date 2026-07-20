# List Stories with Resolved Relations with Storyblok

Retrieves Storyblok stories with resolved relations.

## Endpoint

- **Method:** `GET`
- **Path:** `/stories`
- **Base URL:** `https://api.storyblok.com/v2/cdn`
- **Official documentation:** [List Stories with Resolved Relations](https://www.storyblok.com/docs/api/content-delivery/v2/stories/examples/retrieving-stories-with-resolved-relations)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `resolve_relations` | query | `string` | yes | A comma-separated list of component.field paths to resolve. |
| `version` | query | `string` | no | Whether to read draft or published content. |
