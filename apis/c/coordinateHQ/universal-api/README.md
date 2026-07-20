# <img src="https://mindcloud.imgix.net/apps/icons/coordinatehq_1770211212666.png" alt="CoordinateHQ logo" width="28" height="28"> CoordinateHQ: Universal API

CoordinateHQ through the MindCloud Universal API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/coordinateHQ/latest
- **Actions:** 11
- **OpenAPI specification:** [openapi.json](openapi.json)

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Download Task File](actions/download-task-file.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/coordinateHQ/latest/actions/download-task-file?connectionId=$CONNECTION_ID&project_id=string&task_id=string&file_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (11)

### Entity

| Action | Method | Description |
| --- | --- | --- |
| [List Entity](actions/list-entity.md) | GET |  |

### Groups

| Action | Method | Description |
| --- | --- | --- |
| [List Project Group](actions/list-project-group.md) | GET |  |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [Add Organization Stakeholder](actions/add-organization-stakeholder.md) | POST |  |
| [Add Project to Organization](actions/add-project-to-organization.md) | POST |  |
| [Create Organization](actions/create-organization.md) | POST |  |
| [List Organizations](actions/list-organizations.md) | GET |  |

### Projects

| Action | Method | Description |
| --- | --- | --- |
| [Create Project](actions/create-project.md) | POST |  |
| [List Projects](actions/list-projects.md) | GET |  |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Download Task File](actions/download-task-file.md) | GET |  |
| [List Project Tasks](actions/list-project-tasks.md) | GET |  |
| [Attach Task File](actions/new-action1.md) | POST |  |

