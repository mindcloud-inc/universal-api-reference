# LunaNotes Universal API Sorting

Sortable list actions accept a `sort` query parameter containing a comma-separated list of fields. Prefix a field with `-` for descending order.

`sort=-createdAt,name` sorts by newest first, then by name in ascending order. MindCloud translates this into the sorting format LunaNotes expects, and each action page lists the fields available to sort.

## LunaNotes actions that support sorting

- [List Diagrams](actions/list-diagrams.md)
- [List Flashcard Quizzes](actions/list-flashcard-quizzes.md)
- [List Flashcards](actions/list-flashcards.md)
- [List Note Templates](actions/list-note-templates.md)
- [List Notes](actions/list-notes.md)
- [List Summaries](actions/list-summaries.md)
- [List Tags](actions/list-tags.md)
- [List Transcripts](actions/list-transcripts.md)
- [List Videos](actions/list-videos.md)
