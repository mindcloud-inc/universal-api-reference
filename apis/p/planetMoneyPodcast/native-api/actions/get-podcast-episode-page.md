# Get Podcast Episode Page with Planet Money Podcast

Retrieves a Planet Money episode page from NPR.

## Endpoint

- **Method:** `GET`
- **Path:** `https://www.npr.org/:year/:month/:day/:storyId/:slug`
- **Base URL:** `https://feeds.npr.org/510289`
- **Official documentation:** [Get Podcast Episode Page](https://www.npr.org/2026/03/20/nx-s1-5751177/book-deal-proposal-auction-publishing)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `year` | path | `string` | yes | Four-digit year from the canonical NPR episode URL. |
| `month` | path | `string` | yes | Two-digit month from the canonical NPR episode URL. |
| `day` | path | `string` | yes | Two-digit day from the canonical NPR episode URL. |
| `storyId` | path | `string` | yes | NPR story identifier segment from the canonical episode URL. |
| `slug` | path | `string` | yes | Trailing slug segment from the canonical NPR episode URL. |
