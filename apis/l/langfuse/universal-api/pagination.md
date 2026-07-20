# Langfuse Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Langfuse expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/langfuse/latest/actions/list-annotation-queue-items?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Langfuse actions that support pagination

- [List Annotation Queue Items](actions/list-annotation-queue-items.md)
- [List Annotation Queues](actions/list-annotation-queues.md)
- [List Comments](actions/list-comments.md)
- [List Dataset Items](actions/list-dataset-items.md)
- [List Dataset Run Items](actions/list-dataset-run-items.md)
- [List Dataset Runs](actions/list-dataset-runs.md)
- [List Datasets](actions/list-datasets.md)
- [List Models](actions/list-models.md)
- [List Prompts](actions/list-prompts.md)
- [List Score Configs](actions/list-score-configs.md)
- [List Scores](actions/list-scores.md)
- [List Sessions](actions/list-sessions.md)
- [List Traces](actions/list-traces.md)
