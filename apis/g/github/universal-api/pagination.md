# GitHub Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model GitHub expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/github/latest/actions/get-authenticated-user?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## GitHub actions that support pagination

- [Get Authenticated User](actions/get-authenticated-user.md)
- [List Authenticated User Organizations](actions/list-authenticated-user-organizations.md)
- [List Authenticated User Repositories](actions/list-authenticated-user-repositories.md)
- [List Branches](actions/list-branches.md)
- [List Commits](actions/list-commits.md)
- [List Pull Request Files](actions/list-pull-request-files.md)
- [List Pull Requests](actions/list-pull-requests.md)
- [List Releases](actions/list-releases.md)
- [List Repository Issues](actions/list-repository-issues.md)
- [List Repository Workflow Runs](actions/list-repository-workflow-runs.md)
- [List Repository Workflows](actions/list-repository-workflows.md)
- [Search Issues and Pull Requests](actions/search-issues-and-pull-requests.md)
- [Search Repositories](actions/search-repositories.md)
