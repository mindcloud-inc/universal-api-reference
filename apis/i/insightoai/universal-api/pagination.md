# Insighto.ai Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Insighto.ai expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/insightoai/latest/actions/list-assistants?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Insighto.ai actions that support pagination

- [List Assistants](actions/list-assistants.md)
- [List Contacts](actions/list-contacts.md)
- [List Conversations](actions/list-conversations.md)
- [Get List Of Conversations By Contact Id](actions/list-conversations-by-contact-id.md)
- [List Data Source Files For Data Source Id](actions/list-data-source-files-by-datasource-id.md)
- [List Data Sources](actions/list-data-sources.md)
- [List Intents](actions/list-intents.md)
- [List Widgets](actions/list-widgets.md)
