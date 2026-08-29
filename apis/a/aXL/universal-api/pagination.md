# AXL Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model AXL expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/aXL/latest/actions/get-certificates?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## AXL actions that support pagination

- [Get Certificates](actions/get-certificates.md)
- [Get Contacts](actions/get-contacts.md)
- [Get Course Categories](actions/get-course-categories.md)
- [Get Courses](actions/get-courses.md)
- [Get Libraries](actions/get-libraries.md)
- [Get Orders](actions/get-orders.md)
- [Get Partner Transactions](actions/get-partner-transactions.md)
- [Get Partnership Members](actions/get-partnership-members.md)
- [Get Payments](actions/get-payments.md)
- [Get Products](actions/get-products.md)
- [Get Tasks](actions/get-tasks.md)
