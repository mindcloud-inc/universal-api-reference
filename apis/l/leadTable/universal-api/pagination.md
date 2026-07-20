# LeadTable Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model LeadTable expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/leadTable/latest/actions/list-campaign-leads?connectionId=$CONNECTION_ID&limit=25&offset=0&campaignID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## LeadTable actions that support pagination

- [List campaign leads](actions/list-campaign-leads.md)
- [List customer campaigns](actions/list-customer-campaigns.md)
- [List customers](actions/list-customers.md)
- [Search leads by email](actions/search-leads-by-email.md)
