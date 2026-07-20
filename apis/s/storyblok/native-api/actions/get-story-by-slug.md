# Get Story by Slug with Storyblok

Retrieves a Storyblok story by slug.

## Endpoint

- **Method:** `GET`
- **Path:** `/stories/:storyId`
- **Base URL:** `https://api.storyblok.com/v2/cdn`
- **Official documentation:** [Get Story by Slug](https://www.storyblok.com/docs/api/content-delivery/v2/stories/retrieve-a-single-story)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `storyId` | path | `string` | yes | The story slug or ID to retrieve. |
| `version` | query | `string` | no | Whether to read draft or published content. |
