# Reteach Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Reteach expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/reteach/latest/actions/list-course-invitations?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Reteach actions that support pagination

- [List Course Invitations](actions/list-course-invitations.md)
- [List Courses](actions/list-courses.md)
- [List Customer Course Certificates](actions/list-customer-course-certificates.md)
- [List Customer Exports](actions/list-customer-exports.md)
- [List Customer Groups](actions/list-customer-groups.md)
- [List Customer Imports](actions/list-customer-imports.md)
- [List Customers](actions/list-customers.md)
- [List E-Commerce Orders](actions/list-e-commerce-orders.md)
- [List Participations](actions/list-participations.md)
- [List Tags](actions/list-tags.md)
