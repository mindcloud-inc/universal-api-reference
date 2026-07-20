# Superthread: Native API Reference

A consolidated summary of Superthread's API configuration and 41 documented operations, with links to official documentation.

- **Official docs:** https://superthread.com/docs/api-docs/auth
- **API base URL:** `https://api.superthread.com/v1`

## Authentication

### Personal Access Token

Connect Superthread with a personal access token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://superthread.com/docs/api-docs/auth)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `user`. The next-page cursor is read from `cursor`.

## Pagination

Use `count` in the query string to set the page size. Use `cursor` in the query string as the pagination cursor.

## Endpoints (41 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Add Member to Space](actions/add-member-to-space.md) | `POST /:team_id/projects/:project_id/members` | [docs](https://superthread.com/docs/api-docs/spaces/add-member-to-a-space) |
| [Archive Card](actions/archive-card.md) | `PATCH /:team_id/cards/:card_id` | [docs](https://superthread.com/docs/api-docs/cards/archive-a-card) |
| [Archive Project](actions/archive-project.md) | `PATCH /:team_id/epics/:epic_id` | [docs](https://superthread.com/docs/api-docs/projects/archive-a-project) |
| [Create Board](actions/create-board.md) | `POST /:team_id/boards` | [docs](https://superthread.com/docs/api-docs/boards/create-a-board) |
| [Create Card](actions/create-card.md) | `POST /:team_id/cards` | [docs](https://superthread.com/docs/api-docs/cards/create-a-card) |
| [Create Comment](actions/create-comment.md) | `POST /:team_id/comments` | [docs](https://superthread.com/docs/api-docs/comments/create-a-comment) |
| [Create List](actions/create-list.md) | `POST /:team_id/lists` | [docs](https://superthread.com/docs/api-docs/boards/create-a-list) |
| [Create Note](actions/create-note.md) | `POST /:team_id/notes` | [docs](https://superthread.com/docs/api-docs/notes/create-a-note) |
| [Create Page](actions/create-page.md) | `POST /:team_id/pages` | [docs](https://superthread.com/docs/api-docs/pages/create-a-page) |
| [Create Project](actions/create-project.md) | `POST /:team_id/epics` | [docs](https://superthread.com/docs/api-docs/projects/create-a-project) |
| [Create Space](actions/create-space.md) | `POST /:team_id/projects` | [docs](https://superthread.com/docs/api-docs/spaces/create-a-space) |
| [Create Sprint](actions/create-sprint.md) | `POST /:team_id/sprints` | [docs](https://superthread.com/docs/api-docs/sprints/create-a-sprint) |
| [Get Board](actions/get-board.md) | `GET /:team_id/boards/:board_id` | [docs](https://superthread.com/docs/api-docs/boards/get-a-board) |
| [Get Card](actions/get-card.md) | `GET /:team_id/cards/:card_id` | [docs](https://superthread.com/docs/api-docs/cards/get-a-card) |
| [Get Comment](actions/get-comment.md) | `GET /:team_id/comments/:comment_id` | [docs](https://superthread.com/docs/api-docs/comments/get-a-comment) |
| [Get My Account](actions/get-my-account.md) | `GET /users/me` | [docs](https://superthread.com/docs/api-docs/users/get-my-account) |
| [Get Note](actions/get-note.md) | `GET /:team_id/notes/:note_id` | [docs](https://superthread.com/docs/api-docs/notes/get-a-note) |
| [Get Page](actions/get-page.md) | `GET /:team_id/pages/:page_id` | [docs](https://superthread.com/docs/api-docs/pages/get-a-page) |
| [Get Space](actions/get-space.md) | `GET /:team_id/projects/:project_id` | [docs](https://superthread.com/docs/api-docs/spaces/get-a-space) |
| [Get Sprint](actions/get-sprint.md) | `GET /:team_id/sprints/:sprint_id` | [docs](https://superthread.com/docs/api-docs/sprints/get-a-sprint) |
| [Get Sprint Settings](actions/get-sprint-settings.md) | `GET /:team_id/sprints/settings` | [docs](https://superthread.com/docs/api-docs/sprints/get-sprint-settings) |
| [List Boards](actions/list-boards.md) | `GET /:team_id/boards` | [docs](https://superthread.com/docs/api-docs/boards/get-boards) |
| [List Comments for a Resource](actions/list-comments-for-a-resource.md) | `GET /:team_id/comments` | [docs](https://superthread.com/docs/api-docs/comments/get-comments) |
| [List Notes](actions/list-notes.md) | `GET /:team_id/notes` | [docs](https://superthread.com/docs/api-docs/notes/get-notes) |
| [List Pages](actions/list-pages.md) | `GET /:team_id/pages` | [docs](https://superthread.com/docs/api-docs/pages/get-pages) |
| [List Projects](actions/list-projects.md) | `GET /:team_id/epics` | [docs](https://superthread.com/docs/api-docs/projects/get-projects) |
| [List Replies to a Comment](actions/list-replies-to-a-comment.md) | `GET /:team_id/comments/:comment_id/children` | [docs](https://superthread.com/docs/api-docs/comments/get-replies) |
| [List Spaces](actions/list-spaces.md) | `GET /:team_id/projects` | [docs](https://superthread.com/docs/api-docs/spaces/get-spaces) |
| [List Sprints](actions/list-sprints.md) | `GET /:team_id/sprints` | [docs](https://superthread.com/docs/api-docs/sprints/get-sprints) |
| [List Team Members](actions/list-team-members.md) | `GET /teams/:team_id/members` | [docs](https://superthread.com/docs/api-docs/users/get-team-members) |
| [Replace Card Description](actions/replace-card-description.md) | `PUT /:team_id/cards/:card_id/content` | [docs](https://superthread.com/docs/api-docs/cards/replace-a-card-description) |
| [Replace Page Content](actions/replace-page-content.md) | `PATCH /:team_id/pages/:page_id` | [docs](https://superthread.com/docs/api-docs/pages/replace-a-page-content) |
| [Reply to Comment](actions/reply-to-comment.md) | `POST /:team_id/comments/:comment_id/children` | [docs](https://superthread.com/docs/api-docs/comments/reply-to-a-comment) |
| [Search Results](actions/search-results.md) | `GET /:team_id/search` | [docs](https://superthread.com/docs/api-docs/search/get-search-results) |
| [Update Board](actions/update-board.md) | `PATCH /:team_id/boards/:board_id` | [docs](https://superthread.com/docs/api-docs/boards/update-a-board) |
| [Update Card Property](actions/update-card-property.md) | `PATCH /:team_id/cards/:card_id` | [docs](https://superthread.com/docs/api-docs/cards/update-a-card) |
| [Update List](actions/update-list.md) | `PATCH /:team_id/lists/:list_id` | [docs](https://superthread.com/docs/api-docs/boards/update-a-list) |
| [Update My Account](actions/update-my-account.md) | `PATCH /users/:user_id` | [docs](https://superthread.com/docs/api-docs/users/update-my-account) |
| [Update Page Property](actions/update-page-property.md) | `PATCH /:team_id/pages/:page_id` | [docs](https://superthread.com/docs/api-docs/pages/update-a-page) |
| [Update Project](actions/update-project.md) | `PATCH /:team_id/epics/:epic_id` | [docs](https://superthread.com/docs/api-docs/projects/update-a-project) |
| [Update Space](actions/update-space.md) | `PATCH /:team_id/projects/:project_id` | [docs](https://superthread.com/docs/api-docs/spaces/update-a-space) |
