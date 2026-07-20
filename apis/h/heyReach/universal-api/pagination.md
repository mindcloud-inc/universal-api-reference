# Hey Reach Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Hey Reach expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/heyReach/latest/actions/list-campaign-leads?connectionId=$CONNECTION_ID&limit=25&offset=0&campaignId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Hey Reach actions that support pagination

- [List Campaign Leads](actions/list-campaign-leads.md)
- [List Campaigns](actions/list-campaigns.md)
- [List Campaigns For Lead](actions/list-campaigns-for-lead.md)
- [List Companies In List](actions/list-companies-in-list.md)
- [List Conversations](actions/list-conversations.md)
- [List Leads In List](actions/list-leads-in-list.md)
- [List LinkedIn Accounts](actions/list-linked-in-accounts.md)
- [List Lists](actions/list-lists.md)
- [List Lists For Lead](actions/list-lists-for-lead.md)
- [List Webhooks](actions/list-webhooks.md)
