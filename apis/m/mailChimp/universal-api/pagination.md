# Mailchimp Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Mailchimp expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailChimp/latest/actions/list-audience-members?connectionId=$CONNECTION_ID&limit=25&offset=0&list_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Mailchimp actions that support pagination

- [List Audience Members](actions/list-audience-members.md)
- [List Audience Segments](actions/list-audience-segments.md)
- [List Audiences](actions/list-audiences.md)
- [List Campaigns](actions/list-campaigns.md)
- [List Customers](actions/list-customers.md)
- [List E-commerce Stores](actions/list-e-commerce-stores.md)
- [List Member Tags](actions/list-member-tags.md)
- [List Merge Fields](actions/list-merge-fields.md)
- [List Reports](actions/list-reports.md)
- [List Templates](actions/list-templates.md)
