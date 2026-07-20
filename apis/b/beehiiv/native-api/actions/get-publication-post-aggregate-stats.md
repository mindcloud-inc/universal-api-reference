# Get Publication Post Aggregate Stats with Beehiiv

Retrieves aggregate stats for publication posts from Beehiiv.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/publications/:publicationId/posts/aggregate_stats`
- **Base URL:** `https://api.beehiiv.com`
- **Official documentation:** [Get Publication Post Aggregate Stats](https://developers.beehiiv.com/api-reference/posts/aggregate-stats)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `publicationId` | path | `string` | yes | The prefixed ID of the publication object. |
| `audience` | query | `string` | no | Optionally filter the results by audience. |
| `platform` | query | `string` | no | Optionally filter the results by platform. |
| `status` | query | `string` | no | Optionally filter the results by post status. |
| `content_tags[]` | query | `array<string>` | no | Optionally filter posts by content tags. |
| `authors[]` | query | `array<string>` | no | Optionally filter posts by author names. |
| `hidden_from_feed` | query | `string` | no | Optionally filter by hidden_from_feed state. |
