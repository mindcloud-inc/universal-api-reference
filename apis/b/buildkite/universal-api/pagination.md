# Buildkite Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Buildkite expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/buildkite/latest/actions/list-all-builds?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Buildkite actions that support pagination

- [List All Builds](actions/list-all-builds.md)
- [List Build Annotations](actions/list-build-annotations.md)
- [List Build Artifacts](actions/list-build-artifacts.md)
- [List Job Artifacts](actions/list-job-artifacts.md)
- [List Organization Builds](actions/list-organization-builds.md)
- [List Organization Members](actions/list-organization-members.md)
- [List Organizations](actions/list-organizations.md)
- [List Pipeline Builds](actions/list-pipeline-builds.md)
- [List Pipelines](actions/list-pipelines.md)
- [List Team Members](actions/list-team-members.md)
- [List Team Pipelines](actions/list-team-pipelines.md)
- [List Teams](actions/list-teams.md)
