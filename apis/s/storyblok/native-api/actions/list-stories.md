# List Stories with Storyblok

Retrieves stories from Storyblok for the current space.

## Endpoint

- **Method:** `GET`
- **Path:** `/stories`
- **Base URL:** `https://api.storyblok.com/v2/cdn`
- **Official documentation:** [List Stories](https://www.storyblok.com/docs/api/content-delivery/v2/stories/retrieve-multiple-stories)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `version` | query | `string` | no | Whether to read draft or published content. |
