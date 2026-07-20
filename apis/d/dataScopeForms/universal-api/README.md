# <img src="https://images.mindcloud.co/apps/icons/data-scope-forms_1773863218678.png" alt="DataScope Forms logo" width="28" height="28"> DataScope Forms: Universal API

Access DataScope form answers, metadata, locations, lists, task assignments, notifications, and generated files through the public DataScope API.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/dataScopeForms/latest
- **Category:** Business Intelligence / Data Extraction
- **Actions:** 14
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.mydatascope.com/
- **Vendor API docs:** https://dscope.github.io/docs/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Answers](actions/list-answers.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dataScopeForms/latest/actions/list-answers?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (14)

### Locations

| Action | Method | Description |
| --- | --- | --- |
| [Create Location](actions/create-location.md) | POST | Creates a new location in DataScope Forms. |
| [List Locations](actions/list-locations.md) | GET | Retrieves locations from DataScope Forms. |
| [Update Location](actions/update-location.md) | PUT | Updates an existing location in DataScope Forms. |

### Notifications

| Action | Method | Description |
| --- | --- | --- |
| [List Notifications](actions/list-notifications.md) | GET | Retrieves notifications from DataScope Forms. |

### Tasks

| Action | Method | Description |
| --- | --- | --- |
| [Create Task Assignment](actions/create-task-assignment.md) | POST | Creates a task assignment in DataScope Forms. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Bulk Update List Elements](actions/bulk-update-list-elements.md) | PUT | Updates list elements in DataScope Forms by replacing the full list. |
| [Create List](actions/create-list.md) | POST | Creates a new list in DataScope Forms. |
| [Create List Element](actions/create-list-element.md) | POST | Creates a new list element in DataScope Forms. |
| [Get List Element](actions/get-list-element.md) | GET | Retrieves a list element from DataScope Forms. |
| [List Answers](actions/list-answers.md) | GET | Retrieves submitted answers from DataScope Forms. |
| [List Answers with Metadata](actions/list-answers-with-metadata.md) | GET | Retrieves submitted answers with metadata from DataScope Forms. |
| [List Generated Files](actions/list-generated-files.md) | GET | Retrieves generated files from DataScope Forms. |
| [List List Elements](actions/list-list-elements.md) | GET | Retrieves list elements from DataScope Forms. |
| [Update List Element](actions/update-list-element.md) | PUT | Updates an existing list element in DataScope Forms. |

