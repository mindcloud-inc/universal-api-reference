# CRM in Cloud Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model CRM in Cloud expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cRMInCloud/latest/actions/search-activities?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## CRM in Cloud actions that support pagination

- [Search activities](actions/search-activities.md)
- [Search appointments](actions/search-appointments.md)
- [Search companies](actions/search-companies.md)
- [Search contacts](actions/search-contacts.md)
- [Search leads](actions/search-leads.md)
- [Search lists](actions/search-lists.md)
- [Search opportunities](actions/search-opportunities.md)
- [Search storage items](actions/search-storage-items.md)
