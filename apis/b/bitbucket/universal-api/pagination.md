# Bitbucket Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Bitbucket expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bitbucket/latest/actions/list-branches?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Bitbucket actions that support pagination

- [List Branches](actions/list-branches.md)
- [List Commit Comments](actions/list-commit-comments.md)
- [List Commits](actions/list-commits.md)
- [List My Workspaces](actions/list-my-workspaces.md)
- [List Pipelines](actions/list-pipelines.md)
- [List Project Default Reviewers](actions/list-project-default-reviewers.md)
- [List Projects in Workspace](actions/list-projects-in-workspace.md)
- [List Pull Request Activity](actions/list-pull-request-activity.md)
- [List Pull Request Comments](actions/list-pull-request-comments.md)
- [List Pull Request Statuses](actions/list-pull-request-statuses.md)
- [List Pull Request Tasks](actions/list-pull-request-tasks.md)
- [List Pull Requests](actions/list-pull-requests.md)
- [List Repositories in Workspace](actions/list-repositories-in-workspace.md)
- [List Repository Forks](actions/list-repository-forks.md)
- [List Repository Watchers](actions/list-repository-watchers.md)
- [List Repository Webhooks](actions/list-repository-webhooks.md)
- [List Tags](actions/list-tags.md)
- [List Workspace Members](actions/list-workspace-members.md)
- [List Workspace Permissions](actions/list-workspace-permissions.md)
- [List Workspace Repository Permissions](actions/list-workspace-repository-permissions.md)
