# Calendly Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Calendly expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/calendly/latest/actions/list-event-invitees?connectionId=$CONNECTION_ID&limit=25&offset=0&event_uuid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Calendly actions that support pagination

- [List Event Invitees](actions/list-event-invitees.md)
- [List Event Types](actions/list-event-types.md)
- [List Organization Memberships](actions/list-organization-memberships.md)
- [List Routing Form Submissions](actions/list-routing-form-submissions.md)
- [List Routing Forms](actions/list-routing-forms.md)
- [List Scheduled Events](actions/list-scheduled-events.md)
- [List Webhook Subscriptions](actions/list-webhook-subscriptions.md)
