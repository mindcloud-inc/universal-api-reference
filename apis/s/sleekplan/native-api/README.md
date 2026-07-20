# Sleekplan: Native API Reference

A consolidated summary of Sleekplan's API configuration and 34 documented operations, with links to official documentation.

- **Official docs:** https://sleekplan.com/docs/api/
- **OpenAPI specification:** https://stoplight.io/api/v1/projects/sleekplan/sleekplan-api/nodes/reference/Sleekplan-API.yaml
- **API base URL:** `https://api.sleekplan.com/v1`

## Authentication

### API Key

Use your Sleekplan API key to authenticate REST API requests.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://sleekplan.com/docs/api/)

## API conventions

The current page number is read from `page`.

## Pagination

Use `per_page` in the query string to set the page size (default 10; accepted range 1–100). Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (34 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Comment](actions/create-comment.md) | `POST /post/:postid/comment` | [docs](https://sleekplan.com/docs/api/) |
| [Create NPS Response](actions/create-nps-response.md) | `POST /promoter` | [docs](https://sleekplan.com/docs/api/) |
| [Create or Update Vote](actions/create-or-update-vote.md) | `POST /post/:postid/vote` | [docs](https://sleekplan.com/docs/api/) |
| [Create Post](actions/create-post.md) | `POST /post` | [docs](https://sleekplan.com/docs/api/) |
| [Create Satisfaction Response](actions/create-satisfaction-response.md) | `POST /satisfaction` | [docs](https://sleekplan.com/docs/api/) |
| [Create Update](actions/create-update.md) | `POST /update` | [docs](https://sleekplan.com/docs/api/) |
| [Create Update Satisfaction Response](actions/create-update-satisfaction-response.md) | `POST /update/:updateid/satisfaction` | [docs](https://sleekplan.com/docs/api/) |
| [Create User](actions/create-user.md) | `POST /user` | [docs](https://sleekplan.com/docs/api/) |
| [Delete Comment](actions/delete-comment.md) | `DELETE /post/:postid/comment/:commentid` | [docs](https://sleekplan.com/docs/api/) |
| [Delete Post](actions/delete-post.md) | `DELETE /post/:postid` | [docs](https://sleekplan.com/docs/api/) |
| [Delete Post Metadata](actions/delete-post-metadata.md) | `DELETE /post/:postid/meta/:metakey` | [docs](https://sleekplan.com/docs/api/) |
| [Delete Update](actions/delete-update.md) | `DELETE /update/:updateid` | [docs](https://sleekplan.com/docs/api/) |
| [Delete User](actions/delete-user.md) | `DELETE /user/:userid` | [docs](https://sleekplan.com/docs/api/) |
| [Edit Update](actions/edit-update.md) | `PUT /update/:updateid` | [docs](https://sleekplan.com/docs/api/) |
| [Get Comment](actions/get-comment.md) | `GET /post/:postid/comment/:commentid` | [docs](https://sleekplan.com/docs/api/) |
| [Get Post](actions/get-post.md) | `GET /post/:postid` | [docs](https://sleekplan.com/docs/api/) |
| [Get Post Metadata](actions/get-post-metadata.md) | `GET /post/:postid/meta` | [docs](https://sleekplan.com/docs/api/) |
| [Get Unread Notification Count](actions/get-unread-notification-count.md) | `GET /user/:userid/notifications/count` | [docs](https://sleekplan.com/docs/api/) |
| [Get Update](actions/get-update.md) | `GET /update/:updateid` | [docs](https://sleekplan.com/docs/api/) |
| [Get User](actions/get-user.md) | `GET /user/:userid` | [docs](https://sleekplan.com/docs/api/) |
| [Like Comment](actions/like-comment.md) | `POST /post/:postid/comment/:commentid/like` | [docs](https://sleekplan.com/docs/api/) |
| [List Comments](actions/list-comments.md) | `GET /post/:postid/comments` | [docs](https://sleekplan.com/docs/api/) |
| [List NPS Responses](actions/list-nps-responses.md) | `GET /promoter` | [docs](https://sleekplan.com/docs/api/) |
| [List Posts](actions/list-posts.md) | `GET /posts` | [docs](https://sleekplan.com/docs/api/) |
| [List Satisfaction Responses](actions/list-satisfaction-responses.md) | `GET /satisfaction` | [docs](https://sleekplan.com/docs/api/) |
| [List Update Satisfaction Responses](actions/list-update-satisfaction-responses.md) | `GET /update/:updateid/satisfaction` | [docs](https://sleekplan.com/docs/api/) |
| [List Updates](actions/list-updates.md) | `GET /updates` | [docs](https://sleekplan.com/docs/api/) |
| [List Users](actions/list-users.md) | `GET /users` | [docs](https://sleekplan.com/docs/api/) |
| [List Votes](actions/list-votes.md) | `GET /post/:postid/votes` | [docs](https://sleekplan.com/docs/api/) |
| [Send Content to Intelligence Queue](actions/send-content-to-intelligence-queue.md) | `POST /intelligence/queue` | [docs](https://sleekplan.com/docs/api/) |
| [Update Comment](actions/update-comment.md) | `PUT /post/:postid/comment/:commentid` | [docs](https://sleekplan.com/docs/api/) |
| [Update Post](actions/update-post.md) | `PUT /post/:postid` | [docs](https://sleekplan.com/docs/api/) |
| [Update Post Metadata](actions/update-post-metadata.md) | `PUT /post/:postid/meta` | [docs](https://sleekplan.com/docs/api/) |
| [Update User](actions/update-user.md) | `PUT /user/:userid` | [docs](https://sleekplan.com/docs/api/) |
