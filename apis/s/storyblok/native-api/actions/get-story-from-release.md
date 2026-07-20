# Get Story from Release with Storyblok

Retrieves a Storyblok story from a specific release.

## Endpoint

- **Method:** `GET`
- **Path:** `/stories/:storyId`
- **Base URL:** `https://api.storyblok.com/v2/cdn`
- **Official documentation:** [Get Story from Release](https://www.storyblok.com/docs/api/content-delivery/v2/stories/examples/retrieving-a-story-from-a-specific-release)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `storyId` | path | `string` | yes | The story slug or ID to retrieve from a release. |
| `from_release` | query | `string` | yes | The release ID to read the story from. |
| `version` | query | `string` | no | Whether to read draft or published content. |
