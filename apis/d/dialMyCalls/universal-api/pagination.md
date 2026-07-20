# DialMyCalls Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model DialMyCalls expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dialMyCalls/latest/actions/list-caller-ids?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## DialMyCalls actions that support pagination

- [List Caller IDs](actions/list-caller-ids.md)
- [List Calls](actions/list-calls.md)
- [List Contacts](actions/list-contacts.md)
- [List Contacts in Group](actions/list-contacts-in-group.md)
- [List Groups](actions/list-groups.md)
- [List Keywords](actions/list-keywords.md)
- [List Recordings](actions/list-recordings.md)
- [List Texts](actions/list-texts.md)
- [List Vanity Numbers](actions/list-vanity-numbers.md)
