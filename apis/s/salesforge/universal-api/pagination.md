# Salesforge Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Salesforge expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/salesforge/latest/actions/get-sequence-contact-sending-data?connectionId=$CONNECTION_ID&limit=25&offset=0&workspaceID=wks_989gtkhm1ir6z8hdv3gjn" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Salesforge actions that support pagination

- [Get Sequence Contact Sending Data](actions/get-sequence-contact-sending-data.md)
- [List Contacts](actions/list-contacts.md)
- [List Custom Variables](actions/list-custom-variables.md)
- [List Mailboxes](actions/list-mailboxes.md)
- [List Primebox Labels](actions/list-primebox-labels.md)
- [List Products](actions/list-products.md)
- [List Webhooks](actions/list-webhooks.md)
- [List Workspace Sequences](actions/list-workspace-sequences.md)
- [List Workspace Threads](actions/list-workspace-threads.md)
