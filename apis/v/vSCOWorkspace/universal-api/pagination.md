# VSCO Workspace Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model VSCO Workspace expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vSCOWorkspace/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## VSCO Workspace actions that support pagination

- [List Contacts](actions/list-contacts.md)
- [List Events](actions/list-events.md)
- [List Files](actions/list-files.md)
- [List Galleries](actions/list-galleries.md)
- [List Jobs](actions/list-jobs.md)
- [List Orders](actions/list-orders.md)
- [List Orders for Job](actions/list-orders-for-job.md)
- [List Payments](actions/list-payments.md)
- [List Payments for Job](actions/list-payments-for-job.md)
