# Enrich.so Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Enrich.so expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/enrich/latest/actions/get-batch-finder-results?connectionId=$CONNECTION_ID&limit=25&offset=0&batchId=665a1f4e2c3b7800129dce01" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Enrich.so actions that support pagination

- [Get Batch Finder Results](actions/get-batch-finder-results.md)
- [Get Batch Validation Results](actions/get-batch-validation-results.md)
- [Get Bulk Lookup Results](actions/get-bulk-lookup-results.md)
- [Get Bulk Phone Lookup Results](actions/get-bulk-phone-lookup-results.md)
- [Get Transaction History](actions/get-transaction-history.md)
- [List Reveal Or Enrich Jobs](actions/list-reveal-or-enrich-jobs.md)
