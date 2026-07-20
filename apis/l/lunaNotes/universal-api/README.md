# <img src="https://images.mindcloud.co/apps/icons/lunanotes_1775494552798.png" alt="LunaNotes logo" width="28" height="28"> LunaNotes: Universal API

Manage LunaNotes notes, videos, summaries, flashcards, and diagrams

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/lunaNotes/latest
- **Category:** Productivity / Knowledge Management
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://lunanotes.io
- **Vendor API docs:** https://lunanotes.io/docs

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Notes](actions/list-notes.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lunaNotes/latest/actions/list-notes?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Get Diagram](actions/get-diagram.md) | GET | Retrieves a diagram from LunaNotes. |
| [Get Summary](actions/get-summary.md) | GET | Retrieves a summary from LunaNotes. |
| [Get Transcript](actions/get-transcript.md) | GET | Retrieves a transcript from LunaNotes. |
| [List Diagrams](actions/list-diagrams.md) | GET | Retrieves diagrams from LunaNotes. |
| [List Summaries](actions/list-summaries.md) | GET | Retrieves summaries from LunaNotes. |
| [List Transcripts](actions/list-transcripts.md) | GET | Retrieves transcripts from LunaNotes. |

### Items

| Action | Method | Description |
| --- | --- | --- |
| [Get Flashcard](actions/get-flashcard.md) | GET | Retrieves a flashcard from LunaNotes. |
| [Get Flashcard Quiz](actions/get-flashcard-quiz.md) | GET | Retrieves a flashcard quiz from LunaNotes. |
| [List Flashcard Quizzes](actions/list-flashcard-quizzes.md) | GET | Retrieves flashcard quizzes from LunaNotes. |
| [List Flashcards](actions/list-flashcards.md) | GET | Retrieves flashcards from LunaNotes. |

### Notes

| Action | Method | Description |
| --- | --- | --- |
| [Get Note](actions/get-note.md) | GET | Retrieves a note from LunaNotes. |
| [List Notes](actions/list-notes.md) | GET | Retrieves notes from LunaNotes. |

### Recordings

| Action | Method | Description |
| --- | --- | --- |
| [Get Video](actions/get-video.md) | GET | Retrieves a video from LunaNotes. |
| [List Videos](actions/list-videos.md) | GET | Retrieves videos from LunaNotes. |

### Statuses

| Action | Method | Description |
| --- | --- | --- |
| [Health Check](actions/health-check.md) | GET | Retrieves API health status from LunaNotes. |

### Tags

| Action | Method | Description |
| --- | --- | --- |
| [Get Tag](actions/get-tag.md) | GET | Retrieves a tag from LunaNotes. |
| [List Tags](actions/list-tags.md) | GET | Retrieves tags from LunaNotes. |

### Templates

| Action | Method | Description |
| --- | --- | --- |
| [Get Note Template](actions/get-note-template.md) | GET | Retrieves a note template from LunaNotes. |
| [List Note Templates](actions/list-note-templates.md) | GET | Retrieves note templates from LunaNotes. |

### Users

| Action | Method | Description |
| --- | --- | --- |
| [Get Current User](actions/get-current-user.md) | GET | Retrieves the current user from LunaNotes. |

