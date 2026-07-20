# Firebase Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Firebase expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/firebase/latest/actions/list-android-apps?connectionId=$CONNECTION_ID&limit=25&offset=0&projectId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Firebase actions that support pagination

- [List Android Apps](actions/list-android-apps.md)
- [List Available Projects](actions/list-available-projects.md)
- [List Firebase Projects](actions/list-firebase-projects.md)
- [List iOS Apps](actions/list-ios-apps.md)
- [List Web Apps](actions/list-web-apps.md)
- [Search Project Apps](actions/search-project-apps.md)
