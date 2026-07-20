# Codemagic Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Codemagic expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/codemagic/latest/actions/get-build-actions?connectionId=$CONNECTION_ID&limit=25&offset=0&buildId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Codemagic actions that support pagination

- [Get Build Actions](actions/get-build-actions.md)
- [List App Tester Groups](actions/list-app-tester-groups.md)
- [List App Variable Groups](actions/list-app-variable-groups.md)
- [List Authenticated User Apps](actions/list-authenticated-user-apps.md)
- [List Authenticated User Teams](actions/list-authenticated-user-teams.md)
- [List OTA Projects](actions/list-ota-projects.md)
- [List Team App Previews](actions/list-team-app-previews.md)
- [List Team Apps](actions/list-team-apps.md)
- [List Team Members](actions/list-team-members.md)
- [List Team Variable Groups](actions/list-team-variable-groups.md)
- [List Tester Group Contacts](actions/list-tester-group-contacts.md)
- [List User Notifications](actions/list-user-notifications.md)
- [List Variables For Group](actions/list-variables-for-group.md)
