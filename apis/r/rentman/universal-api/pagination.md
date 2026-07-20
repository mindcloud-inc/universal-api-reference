# Rentman Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Rentman expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rentman/latest/actions/list-appointments?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Rentman actions that support pagination

- [List Appointments](actions/list-appointments.md)
- [List Contact Persons](actions/list-contact-persons.md)
- [List Contacts](actions/list-contacts.md)
- [List Crew](actions/list-crew.md)
- [List Crew Rates](actions/list-crew-rates.md)
- [List Equipment](actions/list-equipment.md)
- [List Equipment Serial Numbers](actions/list-equipment-serial-numbers.md)
- [List Invoices](actions/list-invoices.md)
- [List Project Crew](actions/list-project-crew.md)
- [List Project Equipment](actions/list-project-equipment.md)
- [List Project Functions](actions/list-project-functions.md)
- [List Project Subprojects](actions/list-project-subprojects.md)
- [List Projects](actions/list-projects.md)
- [List Vehicles](actions/list-vehicles.md)
