# PBX Yeastar Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model PBX Yeastar expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pBXYeastar/latest/actions/query-company-contact-list?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## PBX Yeastar actions that support pagination

- [Query Company Contact List](actions/query-company-contact-list.md)
- [Query Extension List](actions/query-extension-list.md)
- [Query Phonebook List](actions/query-phonebook-list.md)
- [Query Queue List](actions/query-queue-list.md)
- [Query Trunk List](actions/query-trunk-list.md)
- [Search Company Contacts](actions/search-company-contacts.md)
- [Search Extensions](actions/search-extensions.md)
- [Search Phonebooks](actions/search-phonebooks.md)
- [Search Queues](actions/search-queues.md)
- [Search Trunks](actions/search-trunks.md)
