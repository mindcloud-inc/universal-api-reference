# Get Story Details with All Things Considered Podcast

Retrieves story details from All Things Considered Podcast.

## Endpoint

- **Method:** `GET`
- **Path:** `/:year/:month/:day/:storyId/:slug`
- **Base URL:** `https://www.npr.org`
- **API:** rest
- **Official documentation:** [Get Story Details](https://www.npr.org/2026/04/29/nx-s1-5803566/musk-continued-his-testimony-from-yesterday-in-lawsuit-against-openai)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `year` | path | `string` | yes |
| `month` | path | `string` | yes |
| `day` | path | `string` | yes |
| `storyId` | path | `string` | yes |
| `slug` | path | `string` | yes |
