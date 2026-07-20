# Headless Testing Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Headless Testing expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/headlessTesting/latest/actions/list-builds?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Headless Testing actions that support pagination

- [List Builds](actions/list-builds.md)
- [List Codeless Suites](actions/list-codeless-suites.md)
- [List Codeless Tests](actions/list-codeless-tests.md)
- [List Screenshots](actions/list-screenshots.md)
- [List Storage Files](actions/list-storage-files.md)
- [List Team Users](actions/list-team-users.md)
- [List Tests](actions/list-tests.md)
