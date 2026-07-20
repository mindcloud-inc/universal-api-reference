# MojoTxt Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model MojoTxt expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mojoTxt/latest/actions/export-donations?connectionId=$CONNECTION_ID&limit=25&offset=0&donationIdOrKeyword=string&phoneNumber=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## MojoTxt actions that support pagination

- [Export Donations](actions/export-donations.md)
- [List Donations](actions/list-donations.md)
- [List Message Log](actions/list-message-log.md)
- [List Messages](actions/list-messages.md)
- [List Phone Number Subscribers](actions/list-phone-number-subscribers.md)
- [List Phone Numbers](actions/list-phone-numbers.md)
- [List Subscribers](actions/list-subscribers.md)
- [List Subscription Lists](actions/list-subscription-lists.md)
