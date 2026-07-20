# Shuffle Queued Posts with Tumblr

Shuffles queued posts in a Tumblr blog.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/blog/:blogIdentifier/posts/queue/shuffle`
- **Base URL:** `https://api.tumblr.com`
- **Official documentation:** [Shuffle Queued Posts](https://www.tumblr.com/docs/en/api/v2#postsqueueshuffle---shuffle-queued-posts)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `blogIdentifier` | path | `string` | yes | Any Tumblr blog identifier for the target blog. |
