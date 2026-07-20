# Get Story by UUID with Storyblok

Retrieves a Storyblok story by UUID.

## Endpoint

- **Method:** `GET`
- **Path:** `/stories/:storyId`
- **Base URL:** `https://api.storyblok.com/v2/cdn`
- **Official documentation:** [Get Story by UUID](https://www.storyblok.com/docs/api/content-delivery/v2/stories/retrieve-a-single-story)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `storyId` | path | `string` | yes | The story UUID to retrieve. |
| `version` | query | `string` | no | Whether to read draft or published content. |
