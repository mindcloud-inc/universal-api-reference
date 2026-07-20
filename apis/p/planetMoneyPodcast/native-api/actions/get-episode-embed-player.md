# Get Episode Embed Player with Planet Money Podcast

Retrieves the NPR embed player page for a Planet Money episode.

## Endpoint

- **Method:** `GET`
- **Path:** `https://www.npr.org/player/embed/:storyId/:mediaId`
- **Base URL:** `https://feeds.npr.org/510289`
- **Official documentation:** [Get Episode Embed Player](https://www.npr.org/player/embed/nx-s1-5751177/nx-s1-mx-5751177-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `storyId` | path | `string` | yes | NPR story identifier used by the embed player. |
| `mediaId` | path | `string` | yes | NPR media identifier used by the embed player. |
