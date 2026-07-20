# Sort Stories with Storyblok

Retrieves Storyblok stories sorted by story properties.

## Endpoint

- **Method:** `GET`
- **Path:** `/stories`
- **Base URL:** `https://api.storyblok.com/v2/cdn`
- **Official documentation:** [Sort Stories](https://www.storyblok.com/docs/api/content-delivery/v2/stories/examples/sorting-by-story-object-property)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `sort_by` | query | `string` | yes | The Storyblok sort expression to apply, such as `created_at:desc`. |
| `version` | query | `string` | no | Whether to read draft or published content. |
