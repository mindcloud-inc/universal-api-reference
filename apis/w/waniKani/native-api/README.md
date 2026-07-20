# WaniKani: Native API Reference

A consolidated summary of WaniKani's API configuration and 21 documented operations, with links to official documentation.

- **Official docs:** https://docs.api.wanikani.com/20170710/
- **API base URL:** `https://api.wanikani.com/v2`

## Authentication

### Personal Access Token

Authenticate with a WaniKani personal access token.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://docs.api.wanikani.com/20170710/#authentication)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Response data is read from `data`.

## Pagination

Use `page_after_id` in the query string as the pagination cursor.

## Endpoints (21 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Study Material](actions/create-study-material.md) | `POST /study_materials` | [docs](https://docs.api.wanikani.com/20170710/#create-a-study-material) |
| [Get Assignment](actions/get-assignment.md) | `GET /assignments/[:id]` | [docs](https://docs.api.wanikani.com/20170710/#get-a-specific-assignment) |
| [Get Level Progression](actions/get-level-progression.md) | `GET /level_progressions/:id` | [docs](https://docs.api.wanikani.com/20170710/#get-a-specific-level-progression) |
| [Get Review Statistic](actions/get-review-statistic.md) | `GET /review_statistics/[:id]` | [docs](https://docs.api.wanikani.com/20170710/#get-a-specific-review-statistic) |
| [Get Spaced Repetition System](actions/get-spaced-repetition-system.md) | `GET /spaced_repetition_systems/:id` | [docs](https://docs.api.wanikani.com/20170710/#get-a-specific-spaced-repetition-system) |
| [Get Study Material](actions/get-study-material.md) | `GET /study_materials/[:id]` | [docs](https://docs.api.wanikani.com/20170710/#get-a-specific-study-material) |
| [Get Subject](actions/get-subject.md) | `GET /subjects/:id` | [docs](https://docs.api.wanikani.com/20170710/#get-a-specific-subject) |
| [Get Summary](actions/get-summary.md) | `GET /summary` | [docs](https://docs.api.wanikani.com/20170710/#get-a-summary) |
| [Get User Information](actions/get-user-information.md) | `GET /user` | [docs](https://docs.api.wanikani.com/20170710/#get-user-information) |
| [Get Voice Actor](actions/get-voice-actor.md) | `GET /voice_actors/:id` | [docs](https://docs.api.wanikani.com/20170710/#get-a-specific-voice-actor) |
| [List Assignments](actions/list-assignments.md) | `GET /assignments` | [docs](https://docs.api.wanikani.com/20170710/#get-all-assignments) |
| [List Level Progressions](actions/list-level-progressions.md) | `GET /level_progressions` | [docs](https://docs.api.wanikani.com/20170710/#get-all-level-progressions) |
| [List Resets](actions/list-resets.md) | `GET /resets` | [docs](https://docs.api.wanikani.com/20170710/#get-all-resets) |
| [List Review Statistics](actions/list-review-statistics.md) | `GET /review_statistics` | [docs](https://docs.api.wanikani.com/20170710/#get-all-review-statistics) |
| [List Spaced Repetition Systems](actions/list-spaced-repetition-systems.md) | `GET /spaced_repetition_systems` | [docs](https://docs.api.wanikani.com/20170710/#get-all-spaced-repetition-systems) |
| [List Study Materials](actions/list-study-materials.md) | `GET /study_materials` | [docs](https://docs.api.wanikani.com/20170710/#get-all-study-materials) |
| [List Subjects](actions/list-subjects.md) | `GET /subjects` | [docs](https://docs.api.wanikani.com/20170710/#get-all-subjects) |
| [List Voice Actors](actions/list-voice-actors.md) | `GET /voice_actors` | [docs](https://docs.api.wanikani.com/20170710/#get-all-voice-actors) |
| [Start Assignment](actions/start-assignment.md) | `PUT /assignments/[:id]/start` | [docs](https://docs.api.wanikani.com/20170710/#start-an-assignment) |
| [Update Study Material](actions/update-study-material.md) | `PUT /study_materials/[:id]` | [docs](https://docs.api.wanikani.com/20170710/#update-a-study-material) |
| [Update User Information](actions/update-user-information.md) | `PUT /user` | [docs](https://docs.api.wanikani.com/20170710/#update-user-information) |
