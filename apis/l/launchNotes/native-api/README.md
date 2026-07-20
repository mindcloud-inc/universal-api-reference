# LaunchNotes: Native API Reference

A consolidated summary of LaunchNotes's API configuration and 40 documented operations, with links to official documentation.

- **Official docs:** https://developer.launchnotes.com/index.html
- **API base URL:** `https://app.launchnotes.io`

## Authentication

### API Key

Management API tokens are Contributor-scoped. Public tokens are read-only and belong to the embed REST surface, not this wrapper.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://help.launchnotes.com/en/articles/5129003-getting-started-with-the-api)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Endpoints (40 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Archive Announcement](actions/archive-announcement.md) | `POST /graphql` | [docs](https://developer.launchnotes.com/index.html#mutation-archiveAnnouncement) |
| [Archive Feedback](actions/archive-feedback.md) | `POST /graphql` | [docs](https://developer.launchnotes.com/index.html#mutation-archiveFeedback) |
| [Archive Ideas](actions/archive-ideas.md) | `POST /graphql` | [docs](https://developer.launchnotes.com/index.html#mutation-archiveIdeas) |
| [Archive Work Item](actions/archive-work-item.md) | `POST /graphql` | [docs](https://developer.launchnotes.com/index.html#mutation-archiveWorkItem) |
| [Copy Announcement To Project](actions/copy-announcement-to-project.md) | `POST /graphql` | [docs](https://developer.launchnotes.com/index.html#mutation-copyAnnouncementToProject) |
| [Create AI Announcement](actions/create-ai-announcement.md) | `POST /graphql` | [docs](https://developer.launchnotes.com/index.html#mutation-createAiAnnouncement) |
| [Create Announcement](actions/create-announcement.md) | `POST /graphql` | [docs](https://developer.launchnotes.com/index.html#mutation-createAnnouncement) |
| [Create Feedback](actions/create-feedback.md) | `POST /graphql` | [docs](https://developer.launchnotes.com/index.html#mutation-createFeedback) |
| [Create Idea](actions/create-idea.md) | `POST /graphql` | [docs](https://developer.launchnotes.com/index.html#mutation-createIdea) |
| [Create Stage](actions/create-stage.md) | `POST /graphql` | [docs](https://developer.launchnotes.com/index.html#mutation-createStage) |
| [Create Work Item](actions/create-work-item.md) | `POST /graphql` | [docs](https://developer.launchnotes.com/index.html#mutation-createWorkItem) |
| [Duplicate Announcement](actions/duplicate-announcement.md) | `POST /graphql` | [docs](https://developer.launchnotes.com/index.html#mutation-duplicateAnnouncement) |
| [Get Announcement](actions/get-announcement.md) | `POST /graphql` | [docs](https://developer.launchnotes.com/index.html#query-announcement) |
| [Get Announcement Digest](actions/get-announcement-digest.md) | `POST /graphql` | [docs](https://developer.launchnotes.com/index.html#query-announcementDigest) |
| [Get Feedback](actions/get-feedback.md) | `POST /graphql` | [docs](https://developer.launchnotes.com/index.html#query-feedback) |
| [Get Idea](actions/get-idea.md) | `POST /graphql` | [docs](https://developer.launchnotes.com/index.html#query-idea) |
| [Get Node](actions/get-node.md) | `POST /graphql` | [docs](https://developer.launchnotes.com/index.html#query-node) |
| [Get Project](actions/get-project.md) | `POST /graphql` | [docs](https://developer.launchnotes.com/index.html#query-project) |
| [Get Session](actions/get-session.md) | `POST /graphql` | [docs](https://developer.launchnotes.com/index.html#query-session) |
| [Get Template](actions/get-template.md) | `POST /graphql` | [docs](https://developer.launchnotes.com/index.html#query-template) |
| [Get Viewer](actions/get-viewer.md) | `POST /graphql` | [docs](https://developer.launchnotes.com/index.html#query-viewer) |
| [Get Work Item](actions/get-work-item.md) | `POST /graphql` | [docs](https://developer.launchnotes.com/index.html#query-workItem) |
| [Import Feedback](actions/import-feedback.md) | `POST /graphql` | [docs](https://developer.launchnotes.com/index.html#mutation-importFeedback) |
| [List Nodes](actions/list-nodes.md) | `POST /graphql` | [docs](https://developer.launchnotes.com/index.html#query-nodes) |
| [Promote Idea](actions/promote-idea.md) | `POST /graphql` | [docs](https://developer.launchnotes.com/index.html#mutation-promoteIdea) |
| [Publish Announcement](actions/publish-announcement.md) | `POST /graphql` | [docs](https://developer.launchnotes.com/index.html#mutation-publishAnnouncement) |
| [Publish Work Item](actions/publish-work-item.md) | `POST /graphql` | [docs](https://developer.launchnotes.com/index.html#mutation-publishWorkItem) |
| [Schedule Announcement](actions/schedule-announcement.md) | `POST /graphql` | [docs](https://developer.launchnotes.com/index.html#mutation-scheduleAnnouncement) |
| [Search Project](actions/search-project.md) | `POST /graphql` | [docs](https://developer.launchnotes.com/index.html#query-projectSearch) |
| [Toggle Published Idea](actions/toggle-published-idea.md) | `POST /graphql` | [docs](https://developer.launchnotes.com/index.html#mutation-togglePublishedIdea) |
| [Unarchive Announcement](actions/unarchive-announcement.md) | `POST /graphql` | [docs](https://developer.launchnotes.com/index.html#mutation-unarchiveAnnouncement) |
| [Unarchive Feedback](actions/unarchive-feedback.md) | `POST /graphql` | [docs](https://developer.launchnotes.com/index.html#mutation-unarchiveFeedback) |
| [Unarchive Ideas](actions/unarchive-ideas.md) | `POST /graphql` | [docs](https://developer.launchnotes.com/index.html#mutation-unarchiveIdeas) |
| [Unpublish Announcement](actions/unpublish-announcement.md) | `POST /graphql` | [docs](https://developer.launchnotes.com/index.html#mutation-unpublishAnnouncement) |
| [Unschedule Announcement](actions/unschedule-announcement.md) | `POST /graphql` | [docs](https://developer.launchnotes.com/index.html#mutation-unscheduleAnnouncement) |
| [Update Announcement](actions/update-announcement.md) | `POST /graphql` | [docs](https://developer.launchnotes.com/index.html#mutation-updateAnnouncement) |
| [Update Feedback](actions/update-feedback.md) | `POST /graphql` | [docs](https://developer.launchnotes.com/index.html#mutation-updateFeedback) |
| [Update Idea](actions/update-idea.md) | `POST /graphql` | [docs](https://developer.launchnotes.com/index.html#mutation-updateIdea) |
| [Update Stage](actions/update-stage.md) | `POST /graphql` | [docs](https://developer.launchnotes.com/index.html#mutation-updateStage) |
| [Update Work Item](actions/update-work-item.md) | `POST /graphql` | [docs](https://developer.launchnotes.com/index.html#mutation-updateWorkItem) |
