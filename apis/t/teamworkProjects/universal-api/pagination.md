# Teamwork Projects Universal API Pagination

Paginated list actions accept `limit` and `offset` as query parameters. MindCloud translates them into whatever pagination model Teamwork Projects expects, so the request shape stays the same even when the native API uses pages or cursors.

| Parameter | Description |
| --- | --- |
| `limit` | Maximum number of records to return |
| `offset` | Number of records to skip |

Start with `offset=0`, add `limit` to the offset after each page, and stop when a page returns fewer rows than requested.

## Example

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teamworkProjects/latest/actions/list-comments?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Teamwork Projects actions that support pagination

- [List Comments](actions/list-comments.md)
- [List Companies](actions/list-companies.md)
- [List Messages](actions/list-messages.md)
- [List Milestones](actions/list-milestones.md)
- [List Notebook Versions](actions/list-notebook-versions.md)
- [List Notebooks](actions/list-notebooks.md)
- [List People](actions/list-people.md)
- [List Project Risks](actions/list-project-risks.md)
- [List Project Tasks](actions/list-project-tasks.md)
- [List Project Updates](actions/list-project-updates.md)
- [List Projects](actions/list-projects.md)
- [List Sample Projects](actions/list-sample-projects.md)
- [List Skills](actions/list-skills.md)
- [List Tags](actions/list-tags.md)
- [List Task Comments](actions/list-task-comments.md)
- [List Task Lists](actions/list-task-lists.md)
- [List Task Time Entries](actions/list-task-time-entries.md)
- [List Tasks](actions/list-tasks.md)
- [List Time Entries](actions/list-time-entries.md)
- [List Timesheets](actions/list-timesheets.md)
