# Clio Manage Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Clio Manage expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clio/latest/actions/list-activities?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Clio Manage actions that support pagination

- [List Activities](actions/list-activities.md)
- [List Activity Descriptions](actions/list-activity-descriptions.md)
- [List Activity Rates](actions/list-activity-rates.md)
- [List Allocations](actions/list-allocations.md)
- [List Calendar Entries](actions/list-calendar-entries.md)
- [List Calendars](actions/list-calendars.md)
- [List Contact Email Addresses](actions/list-contact-email-addresses.md)
- [List Contact Phone Numbers](actions/list-contact-phone-numbers.md)
- [List Contacts](actions/list-contacts.md)
- [List Matter Contacts](actions/list-matter-contacts.md)
- [List Matter Stages](actions/list-matter-stages.md)
- [List Matters](actions/list-matters.md)
- [List Notes](actions/list-notes.md)
- [List Tasks](actions/list-tasks.md)
