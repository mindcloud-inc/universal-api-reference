# LaunchDarkly Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model LaunchDarkly expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/launchDarkly/latest/actions/evaluate-flags?connectionId=$CONNECTION_ID&limit=25&offset=0&environmentKey=string&projectKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## LaunchDarkly actions that support pagination

- [Evaluate Flags](actions/evaluate-flags.md)
- [List Environments](actions/list-environments.md)
- [List Feature Flags](actions/list-feature-flags.md)
- [List Members](actions/list-members.md)
- [List Projects](actions/list-projects.md)
- [List Segments](actions/list-segments.md)
