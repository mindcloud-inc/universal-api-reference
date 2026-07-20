# Fingertip Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Fingertip expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fingertip/latest/actions/list-blog-posts?connectionId=$CONNECTION_ID&limit=25&offset=0&siteId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Fingertip actions that support pagination

- [List Blog Posts](actions/list-blog-posts.md)
- [List Bookings](actions/list-bookings.md)
- [List Event Types](actions/list-event-types.md)
- [List Form Responses](actions/list-form-responses.md)
- [List Form Templates](actions/list-form-templates.md)
- [List Invoices](actions/list-invoices.md)
- [List Orders](actions/list-orders.md)
- [List Site Contacts](actions/list-site-contacts.md)
- [List Site Memberships](actions/list-site-memberships.md)
- [List Webhooks](actions/list-webhooks.md)
- [List Workspaces](actions/list-workspaces.md)
