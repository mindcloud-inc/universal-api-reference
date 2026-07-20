# LunaNotes Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model LunaNotes expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lunaNotes/latest/actions/list-diagrams?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## LunaNotes actions that support pagination

- [List Diagrams](actions/list-diagrams.md)
- [List Flashcard Quizzes](actions/list-flashcard-quizzes.md)
- [List Flashcards](actions/list-flashcards.md)
- [List Note Templates](actions/list-note-templates.md)
- [List Notes](actions/list-notes.md)
- [List Summaries](actions/list-summaries.md)
- [List Tags](actions/list-tags.md)
- [List Transcripts](actions/list-transcripts.md)
- [List Videos](actions/list-videos.md)
