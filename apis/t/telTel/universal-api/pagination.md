# TelTel Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model TelTel expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/telTel/latest/actions/list-available-number-price-groups?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## TelTel actions that support pagination

- [List Available Number Price Groups](actions/list-available-number-price-groups.md)
- [List Calls](actions/list-calls.md)
- [List Contact Group Contacts](actions/list-contact-group-contacts.md)
- [List Contact Groups](actions/list-contact-groups.md)
- [List Contacts](actions/list-contacts.md)
- [List Inbound SMS Reports](actions/list-inbound-sms-reports.md)
- [List Phone Numbers](actions/list-phone-numbers.md)
- [List SMS Campaigns](actions/list-sms-campaigns.md)
- [List SMS Reports](actions/list-sms-reports.md)
