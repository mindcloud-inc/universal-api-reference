# RingCentral Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model RingCentral expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ringCentral/latest/actions/list-company-call-records?connectionId=$CONNECTION_ID&limit=25&offset=0&accountId=~" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## RingCentral actions that support pagination

- [List Company Call Records](actions/list-company-call-records.md)
- [List Company Phone Numbers](actions/list-company-phone-numbers.md)
- [List Extension Phone Numbers](actions/list-extension-phone-numbers.md)
- [List Extensions](actions/list-extensions.md)
- [List Messages](actions/list-messages.md)
- [List User Call Records](actions/list-user-call-records.md)
