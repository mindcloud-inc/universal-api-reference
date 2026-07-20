# Vimeo: Native API Reference

A consolidated summary of Vimeo's API configuration and 24 documented operations, with links to official documentation.

- **Official docs:** https://developer.vimeo.com/api/guides/start
- **API base URL:** `https://api.vimeo.com`

## Authentication

### OAuth 2.0

Connect Vimeo with OAuth 2.0

Register an OAuth application with the provider to obtain client credentials and configure its redirect URI.

1. Send the user to https://api.vimeo.com/oauth/authorize to approve access.
2. Exchange the returned authorization code with a POST request to https://api.vimeo.com/oauth/access_token.
3. Send the resulting access token as `Authorization: Bearer <accessToken>` on API requests.

Requested scopes: `public private edit interact delete`.

[Official authentication documentation](https://developer.vimeo.com/api/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Response data is read from `data`. The next-page cursor is read from `paging.next`. The current page number is read from `page`.

## Pagination

Use `per_page` in the query string to set the page size. Use `page` in the query string to choose the page; numbering starts at 1.

## Sorting

Set the sort field with `sort` in the query string. Set the direction separately with `direction`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (24 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Video to Project](actions/add-video-to-project.md) | `PUT /users/:user_id/projects/:project_id/videos/:video_id` | [docs](https://developer.vimeo.com/api/reference/folders#add_video_to_project) |
| [Add Video to Showcase](actions/add-video-to-showcase.md) | `PUT /users/:user_id/albums/:album_id/videos/:video_id` | [docs](https://developer.vimeo.com/api/reference/showcases#add_video_to_showcase) |
| [Delete Video](actions/delete-video.md) | `DELETE /videos/:video_id` | [docs](https://developer.vimeo.com/api/reference/videos#delete_video) |
| [Get Channel](actions/get-channel.md) | `GET /channels/:channel_id` | [docs](https://developer.vimeo.com/api/reference/channels#get_channel) |
| [Get Project](actions/get-project.md) | `GET /users/:user_id/projects/:project_id` | [docs](https://developer.vimeo.com/api/reference/folders#get_project) |
| [Get Showcase](actions/get-showcase.md) | `GET /users/:user_id/albums/:album_id` | [docs](https://developer.vimeo.com/api/reference/showcases#get_showcase) |
| [Get User](actions/get-user.md) | `GET /users/:user_id` | [docs](https://developer.vimeo.com/api/reference/users#get_user) |
| [Get Video](actions/get-video.md) | `GET /videos/:video_id` | [docs](https://developer.vimeo.com/api/reference/videos#get_video) |
| [List Available Video Showcases](actions/list-available-video-showcases.md) | `GET /videos/:video_id/available_albums` | [docs](https://developer.vimeo.com/api/reference/showcases#get_available_video_showcases) |
| [List Channel Videos](actions/list-channel-videos.md) | `GET /channels/:channel_id/videos` | [docs](https://developer.vimeo.com/api/reference/channels#get_channel_videos) |
| [List Channels](actions/list-channels.md) | `GET /channels` | [docs](https://developer.vimeo.com/api/reference/channels#get_channels) |
| [List Comment Replies](actions/list-comment-replies.md) | `GET /videos/:video_id/comments/:comment_id/replies` | [docs](https://developer.vimeo.com/api/reference/videos#get_comment_replies) |
| [List Project Videos](actions/list-project-videos.md) | `GET /users/:user_id/projects/:project_id/videos` | [docs](https://developer.vimeo.com/api/reference/folders#get_project_videos) |
| [List Projects](actions/list-projects.md) | `GET /users/:user_id/projects` | [docs](https://developer.vimeo.com/api/reference/folders#get_projects) |
| [List Showcase Videos](actions/list-showcase-videos.md) | `GET /users/:user_id/albums/:album_id/videos` | [docs](https://developer.vimeo.com/api/reference/showcases#get_showcase_videos) |
| [List Showcases](actions/list-showcases.md) | `GET /users/:user_id/albums` | [docs](https://developer.vimeo.com/api/reference/showcases#get_showcases) |
| [List User Videos](actions/list-user-videos.md) | `GET /users/:user_id/videos` | [docs](https://developer.vimeo.com/api/reference/videos#get_videos) |
| [List Video Comments](actions/list-video-comments.md) | `GET /videos/:video_id/comments` | [docs](https://developer.vimeo.com/api/reference/videos#get_comments) |
| [List Video Tags](actions/list-video-tags.md) | `GET /videos/:video_id/tags` | [docs](https://developer.vimeo.com/api/reference/videos#get_video_tags) |
| [List Videos with Tag](actions/list-videos-with-tag.md) | `GET /tags/:word/videos` | [docs](https://developer.vimeo.com/api/reference/videos#get_videos_with_tag) |
| [Remove Video from Project](actions/remove-video-from-project.md) | `DELETE /users/:user_id/projects/:project_id/videos/:video_id` | [docs](https://developer.vimeo.com/api/reference/folders#remove_video_from_project) |
| [Remove Video from Showcase](actions/remove-video-from-showcase.md) | `DELETE /users/:user_id/albums/:album_id/videos/:video_id` | [docs](https://developer.vimeo.com/api/reference/showcases#remove_video_from_showcase) |
| [Search Videos](actions/search-videos.md) | `GET /videos` | [docs](https://developer.vimeo.com/api/reference/videos#search_videos) |
| [Update Video](actions/update-video.md) | `PATCH /videos/:video_id` | [docs](https://developer.vimeo.com/api/reference/videos#edit_video) |
