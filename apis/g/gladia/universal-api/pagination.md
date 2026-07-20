# Gladia Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Gladia expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gladia/latest/actions/list-job-history?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Gladia actions that support pagination

- [List Job History](actions/list-job-history.md)
- [List Live Jobs](actions/list-live-jobs.md)
- [List Pre-recorded Transcriptions](actions/list-pre-recorded-transcriptions.md)
- [List Transcriptions](actions/list-transcriptions.md)
