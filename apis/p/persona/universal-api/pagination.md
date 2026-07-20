# Persona Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Persona expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/persona/latest/actions/list-accounts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Persona actions that support pagination

- [List Accounts](actions/list-accounts.md)
- [List API keys](actions/list-api-keys.md)
- [List API Logs](actions/list-api-logs.md)
- [List Cases](actions/list-cases.md)
- [List Connections](actions/list-connections.md)
- [List Events](actions/list-events.md)
- [List Importers](actions/list-importers.md)
- [List Inquiries](actions/list-inquiries.md)
- [List Inquiry Templates](actions/list-inquiry-templates.md)
- [List Lists](actions/list-lists.md)
- [List Reports](actions/list-reports.md)
- [List Share Tokens](actions/list-share-tokens.md)
- [List Transactions](actions/list-transactions.md)
- [List User Audit Logs](actions/list-user-audit-logs.md)
- [List Webhooks](actions/list-webhooks.md)
- [List Workflow Runs](actions/list-workflow-runs.md)
- [Search Accounts](actions/search-accounts.md)
- [Search Cases](actions/search-cases.md)
