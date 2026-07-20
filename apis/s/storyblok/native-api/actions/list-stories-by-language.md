# List Stories by Language with Storyblok

Retrieves Storyblok stories in a specific language.

## Endpoint

- **Method:** `GET`
- **Path:** `/stories`
- **Base URL:** `https://api.storyblok.com/v2/cdn`
- **Official documentation:** [List Stories by Language](https://www.storyblok.com/docs/api/content-delivery/v2/stories/examples/retrieving-stories-in-a-particular-language)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `language` | query | `string` | yes | The language code to use when listing stories. |
| `version` | query | `string` | no | Whether to read draft or published content. |
