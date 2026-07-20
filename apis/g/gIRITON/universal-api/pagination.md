# GIRITON Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model GIRITON expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gIRITON/latest/actions/list-agenda-records?connectionId=$CONNECTION_ID&limit=25&offset=0&agendaId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## GIRITON actions that support pagination

- [List Agenda Records](actions/list-agenda-records.md)
- [List Agendas](actions/list-agendas.md)
- [List Attendance Data](actions/list-attendance-data.md)
- [List Closed Attendance](actions/list-closed-attendance.md)
- [List Documents](actions/list-documents.md)
- [List Projects](actions/list-projects.md)
- [List Users Activity](actions/list-users-activity.md)
- [List Users Employed Between Dates](actions/list-users-employed-between-dates.md)
- [List Users Employed On Date](actions/list-users-employed-on-date.md)
