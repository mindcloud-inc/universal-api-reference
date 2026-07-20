# <img src="https://images.mindcloud.co/apps/icons/iris-dfir-icon_1775845066120.png" alt="Iris Dfir logo" width="28" height="28"> Iris Dfir: Universal API

IRIS is an incident response and DFIR collaboration platform for managing cases, alerts, IOCs, assets, evidences, tasks, comments, and related response workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/irisDfir/latest
- **Category:** IT Operations / Security & Compliance
- **Actions:** 22
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.dfir-iris.org/
- **Vendor API docs:** https://docs.dfir-iris.org/latest/operations/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Cases](actions/list-cases.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/irisDfir/latest/actions/list-cases?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (22)

### Alert

| Action | Method | Description |
| --- | --- | --- |
| [List Alerts](actions/list-alerts.md) | GET |  |
| [List Alerts Legacy](actions/list-alerts-legacy.md) | GET |  |

### Assets

| Action | Method | Description |
| --- | --- | --- |
| [Create Asset](actions/create-asset.md) | POST |  |
| [Delete Asset](actions/delete-asset.md) | DELETE |  |
| [Get Asset](actions/get-asset.md) | GET |  |
| [List Assets](actions/list-assets.md) | GET |  |
| [Update Asset](actions/update-asset.md) | PUT |  |

### Cases

| Action | Method | Description |
| --- | --- | --- |
| [Create Case](actions/create-case.md) | POST |  |
| [Delete Case](actions/delete-case.md) | DELETE |  |
| [Get Case](actions/get-case.md) | GET |  |
| [List Cases](actions/list-cases.md) | GET |  |
| [Update Case](actions/update-case.md) | PUT |  |

### Note

| Action | Method | Description |
| --- | --- | --- |
| [List Note Directories](actions/list-note-directories.md) | GET |  |

### Notes

| Action | Method | Description |
| --- | --- | --- |
| [Add Note](actions/add-note.md) | POST |  |
| [Delete Note](actions/delete-note.md) | DELETE |  |
| [Get Note](actions/get-note.md) | GET |  |
| [Update Note](actions/update-note.md) | PUT |  |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Create Task](actions/create-task.md) | POST |  |
| [Delete Task](actions/delete-task.md) | DELETE |  |
| [Get Task](actions/get-task.md) | GET |  |
| [List Tasks](actions/list-tasks.md) | GET |  |
| [Update Task](actions/update-task.md) | PUT |  |

