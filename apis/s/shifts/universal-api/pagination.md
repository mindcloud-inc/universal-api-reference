# 7shifts Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model 7shifts expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shifts/latest/actions/get-user-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## 7shifts actions that support pagination

- [Get User Contacts](actions/get-user-contacts.md)
- [List Departments](actions/list-departments.md)
- [List Employment Records](actions/list-employment-records.md)
- [List Locations](actions/list-locations.md)
- [List Roles](actions/list-roles.md)
- [List Shifts](actions/list-shifts.md)
- [List Time Punches](actions/list-time-punches.md)
- [List Users](actions/list-users.md)
