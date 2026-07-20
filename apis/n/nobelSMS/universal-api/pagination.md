# NobelSMS Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model NobelSMS expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nobelSMS/latest/actions/list-balances?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## NobelSMS actions that support pagination

- [List Balances](actions/list-balances.md)
- [List Blacklist Entries](actions/list-blacklist-entries.md)
- [List Contacts](actions/list-contacts.md)
- [List SMS Templates](actions/list-sms-templates.md)
- [List Tags](actions/list-tags.md)
