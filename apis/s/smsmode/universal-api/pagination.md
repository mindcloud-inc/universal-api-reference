# smsmode Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model smsmode expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smsmode/latest/actions/list-channels?connectionId=$CONNECTION_ID&limit=25&offset=0&organisationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## smsmode actions that support pagination

- [List Channels](actions/list-channels.md)
- [List Consumptions](actions/list-consumptions.md)
- [List Credentials](actions/list-credentials.md)
- [List Organisations](actions/list-organisations.md)
- [List RCS Campaigns](actions/list-rcs-campaigns.md)
- [List RCS Messages](actions/list-rcs-messages.md)
- [List SMS Campaigns](actions/list-sms-campaigns.md)
- [List SMS Messages](actions/list-sms-messages.md)
- [List Transfers](actions/list-transfers.md)
