# LunaNotes: Native API Reference

A consolidated summary of LunaNotes's API configuration and 20 documented operations, with links to official documentation.

- **Official docs:** https://lunanotes.io/docs
- **API base URL:** `https://api.lunanotes.io`

## Authentication

### API Key

Use your LunaNotes API key as a Bearer token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://lunanotes.io/docs/authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

Responses from this API use JSON. Response data is read from `data`.

## Pagination

Use `limit` in the query string to set the page size (default 50; accepted range 1–100). Use `offset` in the query string as the record offset.

## Sorting

Set the sort field with `orderBy` in the query string. Set the direction separately with `orderDirection`. Use `asc` for ascending order and `desc` for descending order. Only one sort field is accepted.

## Endpoints (20 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | `GET /v1/me` | [docs](https://lunanotes.io/docs/me/get-v1-me) |
| [Get Diagram](actions/get-diagram.md) | `GET /v1/diagrams/:id` | [docs](https://lunanotes.io/docs/diagrams/get-v1-diagrams-id) |
| [Get Flashcard](actions/get-flashcard.md) | `GET /v1/flashcards/:id` | [docs](https://lunanotes.io/docs/flashcards/get-v1-flashcards-id) |
| [Get Flashcard Quiz](actions/get-flashcard-quiz.md) | `GET /v1/flashcard-quizzes/:id` | [docs](https://lunanotes.io/docs/flashcard-quizzes/get-v1-flashcard-quizzes-id) |
| [Get Note](actions/get-note.md) | `GET /v1/notes/:id` | [docs](https://lunanotes.io/docs/notes/get-v1-notes-id) |
| [Get Note Template](actions/get-note-template.md) | `GET /v1/note-templates/:id` | [docs](https://lunanotes.io/docs/note-templates/get-v1-note-templates-id) |
| [Get Summary](actions/get-summary.md) | `GET /v1/summaries/:id` | [docs](https://lunanotes.io/docs/summaries/get-v1-summaries-id) |
| [Get Tag](actions/get-tag.md) | `GET /v1/tags/:id` | [docs](https://lunanotes.io/docs/tags/get-v1-tags-id) |
| [Get Transcript](actions/get-transcript.md) | `GET /v1/transcripts/:id` | [docs](https://lunanotes.io/docs/transcripts/get-v1-transcripts-id) |
| [Get Video](actions/get-video.md) | `GET /v1/videos/:id` | [docs](https://lunanotes.io/docs/videos/get-v1-videos-id) |
| [Health Check](actions/health-check.md) | `GET /health-check` | [docs](https://lunanotes.io/docs/index/get-health-check) |
| [List Diagrams](actions/list-diagrams.md) | `GET /v1/diagrams` | [docs](https://lunanotes.io/docs/diagrams/get-v1-diagrams) |
| [List Flashcard Quizzes](actions/list-flashcard-quizzes.md) | `GET /v1/flashcard-quizzes` | [docs](https://lunanotes.io/docs/flashcard-quizzes/get-v1-flashcard-quizzes) |
| [List Flashcards](actions/list-flashcards.md) | `GET /v1/flashcards` | [docs](https://lunanotes.io/docs/flashcards/get-v1-flashcards) |
| [List Note Templates](actions/list-note-templates.md) | `GET /v1/note-templates` | [docs](https://lunanotes.io/docs/note-templates/get-v1-note-templates) |
| [List Notes](actions/list-notes.md) | `GET /v1/notes` | [docs](https://lunanotes.io/docs/notes/get-v1-notes) |
| [List Summaries](actions/list-summaries.md) | `GET /v1/summaries` | [docs](https://lunanotes.io/docs/summaries/get-v1-summaries) |
| [List Tags](actions/list-tags.md) | `GET /v1/tags` | [docs](https://lunanotes.io/docs/tags/get-v1-tags) |
| [List Transcripts](actions/list-transcripts.md) | `GET /v1/transcripts` | [docs](https://lunanotes.io/docs/transcripts/get-v1-transcripts) |
| [List Videos](actions/list-videos.md) | `GET /v1/videos` | [docs](https://lunanotes.io/docs/videos/get-v1-videos) |
