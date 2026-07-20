# <img src="https://images.mindcloud.co/apps/icons/you-tube_1772219925923.png" alt="YouTube logo" width="28" height="28"> YouTube: Universal API

Manage channels, videos, playlists, captions, and thumbnails

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/youtube/latest
- **Category:** Marketing / Social Media
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.youtube.com
- **Vendor API docs:** https://developers.google.com/youtube/v3

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Channels](actions/list-channels.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/youtube/latest/actions/list-channels?connectionId=$CONNECTION_ID&limit=25&offset=0&part=snippet%2CcontentDetails%2Cstatistics" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Activity

| Action | Method | Description |
| --- | --- | --- |
| [List Activities](actions/list-activities.md) | GET | Retrieves channel activity items from YouTube. |

### Caption

| Action | Method | Description |
| --- | --- | --- |
| [List Captions](actions/list-captions.md) | GET | Retrieves caption tracks for a YouTube video. |

### Channel

| Action | Method | Description |
| --- | --- | --- |
| [List Channels](actions/list-channels.md) | GET | Retrieves one or more channels from YouTube. |
| [Update Channel](actions/update-channel.md) | PUT | Updates an existing channel in YouTube. |

### Comment

| Action | Method | Description |
| --- | --- | --- |
| [List Comments](actions/list-comments.md) | GET | Retrieves comments or replies from YouTube. |

### Comment Thread

| Action | Method | Description |
| --- | --- | --- |
| [List Comment Threads](actions/list-comment-threads.md) | GET | Retrieves comment threads for YouTube videos or channels. |

### Playlist

| Action | Method | Description |
| --- | --- | --- |
| [Create Playlist](actions/create-playlist.md) | POST | Creates a new playlist in YouTube. |
| [List Playlists](actions/list-playlists.md) | GET | Retrieves one or more playlists from YouTube. |
| [Update Playlist](actions/update-playlist.md) | PUT | Updates an existing playlist in YouTube. |

### Playlist Item

| Action | Method | Description |
| --- | --- | --- |
| [List Playlist Items](actions/list-playlist-items.md) | GET | Retrieves items from a YouTube playlist. |

### Search Result

| Action | Method | Description |
| --- | --- | --- |
| [Search Videos](actions/search-videos.md) | GET | Searches YouTube for videos by default. |

### Subscription

| Action | Method | Description |
| --- | --- | --- |
| [List Subscriptions](actions/list-subscriptions.md) | GET | Retrieves one or more subscriptions from YouTube. |

### Thumbnail

| Action | Method | Description |
| --- | --- | --- |
| [Set Thumbnail](actions/set-thumbnail.md) | PUT | Sets a custom thumbnail for a YouTube video. |

### Video

| Action | Method | Description |
| --- | --- | --- |
| [Delete Video](actions/delete-video.md) | DELETE | Deletes an existing video from YouTube. |
| [Get Video Rating](actions/get-video-rating.md) | GET | Retrieves the authenticated user's rating for YouTube videos. |
| [List Videos](actions/list-videos.md) | GET | Retrieves one or more videos from YouTube. |
| [Rate Video](actions/rate-video.md) | PUT | Sets the authenticated user's rating for a YouTube video. |
| [Update Video](actions/update-video.md) | PUT | Updates an existing video in YouTube. |
| [Upload Video](actions/upload-video.md) | POST | Uploads a new video to YouTube. |

### Video Category

| Action | Method | Description |
| --- | --- | --- |
| [List Video Categories](actions/list-video-categories.md) | GET | Retrieves available video categories from YouTube. |

