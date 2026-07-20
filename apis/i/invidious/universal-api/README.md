# <img src="https://images.mindcloud.co/apps/icons/invidious_1776179192415.png" alt="Invidious logo" width="28" height="28"> Invidious: Universal API

Use Invidious to search, inspect, and manage YouTube-style video data through a selected Invidious instance.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/invidious/latest
- **Category:** Marketing / Social Media
- **Actions:** 40
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://invidious.io/
- **Vendor API docs:** https://docs.invidious.io/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Stats](actions/get-stats.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/invidious/latest/actions/get-stats?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (40)

### Caption

| Action | Method | Description |
| --- | --- | --- |
| [Get Video Captions](actions/get-video-captions.md) | GET |  |

### Channel

| Action | Method | Description |
| --- | --- | --- |
| [Get Channel](actions/get-channel.md) | GET |  |
| [Get Channel Related Channels](actions/get-channel-related-channels.md) | GET |  |

### Clip

| Action | Method | Description |
| --- | --- | --- |
| [Get Clip](actions/get-clip.md) | GET |  |

### Comment Thread

| Action | Method | Description |
| --- | --- | --- |
| [Get Community Post Comments](actions/get-community-post-comments.md) | GET |  |
| [Get Video Comments](actions/get-video-comments.md) | GET |  |

### Community Post

| Action | Method | Description |
| --- | --- | --- |
| [Get Channel Community](actions/get-channel-community.md) | GET |  |
| [Get Community Post](actions/get-community-post.md) | GET |  |

### Feed

| Action | Method | Description |
| --- | --- | --- |
| [Get Auth Feed](actions/get-auth-feed.md) | GET |  |

### Hashtag Result

| Action | Method | Description |
| --- | --- | --- |
| [Get Hashtag Results](actions/get-hashtag-results.md) | GET |  |

### Instance Stats

| Action | Method | Description |
| --- | --- | --- |
| [Get Stats](actions/get-stats.md) | GET |  |

### Mix

| Action | Method | Description |
| --- | --- | --- |
| [Get Mix](actions/get-mix.md) | GET |  |

### Playlist

| Action | Method | Description |
| --- | --- | --- |
| [Create Auth Playlist](actions/create-auth-playlist.md) | POST |  |
| [Delete Auth Playlist](actions/delete-auth-playlist.md) | DELETE |  |
| [Get Auth Playlist](actions/get-auth-playlist.md) | GET |  |
| [Get Channel Playlists](actions/get-channel-playlists.md) | GET |  |
| [Get Playlist](actions/get-playlist.md) | GET |  |
| [List Auth Playlists](actions/list-auth-playlists.md) | GET |  |
| [Update Auth Playlist](actions/update-auth-playlist.md) | PUT |  |

### Playlist Video

| Action | Method | Description |
| --- | --- | --- |
| [Add Video To Auth Playlist](actions/add-video-to-auth-playlist.md) | POST |  |
| [Remove Video From Auth Playlist](actions/remove-video-from-auth-playlist.md) | DELETE |  |

### Podcast

| Action | Method | Description |
| --- | --- | --- |
| [Get Channel Podcasts](actions/get-channel-podcasts.md) | GET |  |

### Preference

| Action | Method | Description |
| --- | --- | --- |
| [Get Auth Preferences](actions/get-auth-preferences.md) | GET |  |
| [Update Auth Preferences](actions/update-auth-preferences.md) | PUT |  |

### Release

| Action | Method | Description |
| --- | --- | --- |
| [Get Channel Releases](actions/get-channel-releases.md) | GET |  |

### Resolved Url

| Action | Method | Description |
| --- | --- | --- |
| [Resolve URL](actions/resolve-url.md) | GET |  |

### Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Search Channel](actions/search-channel.md) | GET |  |
| [Search Videos And Channels](actions/search-videos-and-channels.md) | GET |  |

### Search Suggestion

| Action | Method | Description |
| --- | --- | --- |
| [Get Search Suggestions](actions/get-search-suggestions.md) | GET |  |

### Short Video

| Action | Method | Description |
| --- | --- | --- |
| [Get Channel Shorts](actions/get-channel-shorts.md) | GET |  |

### Stream

| Action | Method | Description |
| --- | --- | --- |
| [Get Channel Streams](actions/get-channel-streams.md) | GET |  |

### Subscription

| Action | Method | Description |
| --- | --- | --- |
| [Add Auth Subscription](actions/add-auth-subscription.md) | POST |  |
| [List Auth Subscriptions](actions/list-auth-subscriptions.md) | GET |  |
| [Remove Auth Subscription](actions/remove-auth-subscription.md) | DELETE |  |

### Video

| Action | Method | Description |
| --- | --- | --- |
| [Get Channel Latest Videos](actions/get-channel-latest-videos.md) | GET |  |
| [Get Channel Videos](actions/get-channel-videos.md) | GET |  |
| [Get Popular Videos](actions/get-popular-videos.md) | GET |  |
| [Get Trending Videos](actions/get-trending-videos.md) | GET |  |
| [Get Video](actions/get-video.md) | GET |  |

### Video Annotation

| Action | Method | Description |
| --- | --- | --- |
| [Get Video Annotations](actions/get-video-annotations.md) | GET |  |

