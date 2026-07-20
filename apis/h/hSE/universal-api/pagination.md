# 4HSE Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model 4HSE expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hSE/latest/actions/list-action-sessions?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## 4HSE actions that support pagination

- [List Action Sessions](actions/list-action-sessions.md)
- [List Action Subscriptions](actions/list-action-subscriptions.md)
- [List Actions](actions/list-actions.md)
- [List Certificate Action Links](actions/list-certificate-action-links.md)
- [List Certificates](actions/list-certificates.md)
- [List Equipment](actions/list-equipment.md)
- [List Incidents](actions/list-incidents.md)
- [List Offices](actions/list-offices.md)
- [List People](actions/list-people.md)
- [List PersonOffice Assignments](actions/list-person-office-assignments.md)
- [List Projects](actions/list-projects.md)
- [List Session Subscriptions](actions/list-session-subscriptions.md)
- [List Work Groups](actions/list-work-groups.md)
