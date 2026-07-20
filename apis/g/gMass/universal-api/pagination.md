# GMass Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model GMass expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gMass/latest/actions/list-campaign-blocks?connectionId=$CONNECTION_ID&limit=25&offset=0&campaignId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## GMass actions that support pagination

- [List Campaign Blocks](actions/list-campaign-blocks.md)
- [List Campaign Bounces](actions/list-campaign-bounces.md)
- [List Campaign Clicks](actions/list-campaign-clicks.md)
- [List Campaign Opens](actions/list-campaign-opens.md)
- [List Campaign Recipients](actions/list-campaign-recipients.md)
- [List Campaign Replies](actions/list-campaign-replies.md)
- [List Campaign Unsubscribes](actions/list-campaign-unsubscribes.md)
- [List Campaigns](actions/list-campaigns.md)
- [List Email Lists](actions/list-email-lists.md)
