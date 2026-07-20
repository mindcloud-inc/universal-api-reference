# <img src="https://images.mindcloud.co/apps/icons/vimeo_1773247211690.png" alt="Vimeo logo" width="28" height="28"> Vimeo: Universal API

Manage Vimeo videos, uploads, folders, and playback

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/vimeo/latest
- **Category:** Communication / Video Communications
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://vimeo.com
- **Vendor API docs:** https://developer.vimeo.com/api/guides/start

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Channel](actions/get-channel.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vimeo/latest/actions/get-channel?connectionId=$CONNECTION_ID&channelId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Channel

| Action | Method | Description |
| --- | --- | --- |
| [Get Channel](actions/get-channel.md) | GET | Retrieves a channel record from Vimeo. |
| [List Channels](actions/list-channels.md) | GET | Retrieves channel records from the Vimeo API. |

### Comment

| Action | Method | Description |
| --- | --- | --- |
| [List Comment Replies](actions/list-comment-replies.md) | GET | Retrieves replies to a Vimeo video comment. |
| [List Video Comments](actions/list-video-comments.md) | GET | Retrieves comments on a Vimeo video. |

### Folder

| Action | Method | Description |
| --- | --- | --- |
| [Get Project](actions/get-project.md) | GET | Retrieves a project record from Vimeo. |
| [List Projects](actions/list-projects.md) | GET | Retrieves a user's projects from Vimeo. |

### Showcase

| Action | Method | Description |
| --- | --- | --- |
| [Add Video to Showcase](actions/add-video-to-showcase.md) | POST | Adds a video to a showcase in Vimeo. |
| [Get Showcase](actions/get-showcase.md) | GET | Retrieves a showcase record from Vimeo. |
| [List Available Video Showcases](actions/list-available-video-showcases.md) | GET | Retrieves showcases available for a Vimeo video. |
| [List Showcases](actions/list-showcases.md) | GET | Retrieves a user's showcases from Vimeo. |
| [Remove Video from Showcase](actions/remove-video-from-showcase.md) | DELETE | Deletes a video from a showcase in Vimeo. |

### Tag

| Action | Method | Description |
| --- | --- | --- |
| [List Video Tags](actions/list-video-tags.md) | GET | Retrieves tags for a Vimeo video. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get User](actions/get-user.md) | GET | Retrieves a user record from Vimeo. |

### Video

| Action | Method | Description |
| --- | --- | --- |
| [Add Video to Project](actions/add-video-to-project.md) | POST | Adds a video to a project in Vimeo. |
| [Delete Video](actions/delete-video.md) | DELETE | Deletes an existing video from Vimeo. |
| [Get Video](actions/get-video.md) | GET | Retrieves a video record from Vimeo. |
| [List Channel Videos](actions/list-channel-videos.md) | GET | Retrieves videos in a Vimeo channel. |
| [List Project Videos](actions/list-project-videos.md) | GET | Retrieves videos in a Vimeo project. |
| [List Showcase Videos](actions/list-showcase-videos.md) | GET | Retrieves videos in a Vimeo showcase. |
| [List User Videos](actions/list-user-videos.md) | GET | Retrieves a user's uploaded videos from Vimeo. |
| [List Videos with Tag](actions/list-videos-with-tag.md) | GET | Retrieves videos with a specific tag from Vimeo. |
| [Remove Video from Project](actions/remove-video-from-project.md) | DELETE | Deletes a video from a project in Vimeo. |
| [Search Videos](actions/search-videos.md) | GET | Finds videos in Vimeo by search query. |
| [Update Video](actions/update-video.md) | PUT | Updates an existing video in Vimeo. |

