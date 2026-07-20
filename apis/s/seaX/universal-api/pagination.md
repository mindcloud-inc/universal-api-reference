# SeaX Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model SeaX expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/seaX/latest/actions/list-auto-dialer-campaign-logs?connectionId=$CONNECTION_ID&limit=25&offset=0&autoDialerCampaignId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## SeaX actions that support pagination

- [List Auto Dialer Campaign Logs](actions/list-auto-dialer-campaign-logs.md)
- [List Auto Dialer Campaigns](actions/list-auto-dialer-campaigns.md)
- [List Campaign Logs](actions/list-campaign-logs.md)
- [List Campaigns](actions/list-campaigns.md)
- [List Contacts](actions/list-contacts.md)
- [List Conversations](actions/list-conversations.md)
