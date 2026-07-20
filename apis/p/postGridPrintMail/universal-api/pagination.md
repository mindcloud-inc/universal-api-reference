# PostGrid Print & Mail Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model PostGrid Print & Mail expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/postGridPrintMail/latest/actions/list-bank-accounts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## PostGrid Print & Mail actions that support pagination

- [List Bank Accounts](actions/list-bank-accounts.md)
- [List Cheques](actions/list-cheques.md)
- [List Contacts](actions/list-contacts.md)
- [List Letters](actions/list-letters.md)
- [List Postcards](actions/list-postcards.md)
- [List Templates](actions/list-templates.md)
