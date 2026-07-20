# DirectIQ Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model DirectIQ expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/directiq/latest/actions/get-bounce-report?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## DirectIQ actions that support pagination

- [Get bounce report](actions/get-bounce-report.md)
- [Get click report](actions/get-click-report.md)
- [Get complaint report](actions/get-complaint-report.md)
- [Get domain report](actions/get-domain-report.md)
- [Get email client report](actions/get-email-client-report.md)
- [Get open report](actions/get-open-report.md)
- [Get opens from social media campaign](actions/get-opens-from-social-media-campaign.md)
- [Get recipient report](actions/get-recipient-report.md)
- [Get unsubscribe report](actions/get-unsubscribe-report.md)
- [List Contacts](actions/list-contacts.md)
