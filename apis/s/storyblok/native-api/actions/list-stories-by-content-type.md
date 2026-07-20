# List Stories by Content Type with Storyblok

Retrieves Storyblok stories for a specific content type.

## Endpoint

- **Method:** `GET`
- **Path:** `/stories`
- **Base URL:** `https://api.storyblok.com/v2/cdn`
- **Official documentation:** [List Stories by Content Type](https://www.storyblok.com/docs/api/content-delivery/v2/stories/retrieve-multiple-stories)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `content_type` | query | `string` | yes | Only return stories for this Storyblok component type. |
