# <img src="https://images.mindcloud.co/apps/icons/images_1774543881490.png" alt="Workiom logo" width="28" height="28"> Workiom: Universal API

Production-ready wrapper for the Workiom API key REST API, covering apps, lists, fields, views, and records.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/workiom/latest
- **Category:** Content & Files / Storage
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.workiom.com
- **Vendor API docs:** https://api.workiom.com/swagger/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Apps](actions/list-apps.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/workiom/latest/actions/list-apps?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Apps

| Action | Method | Description |
| --- | --- | --- |
| [Get App](actions/get-app.md) | GET | Retrieves an app from your Workiom workspace. |
| [List Apps](actions/list-apps.md) | GET | Retrieves apps from your Workiom workspace. |

### Fields

| Action | Method | Description |
| --- | --- | --- |
| [Create Field](actions/create-field.md) | POST | Creates a new custom field in Workiom. |
| [Get Field](actions/get-field.md) | GET | Retrieves a custom field from your Workiom workspace. |
| [List Fields](actions/list-fields.md) | GET | Retrieves custom fields from your Workiom workspace. |
| [Update Field](actions/update-field.md) | PUT | Updates an existing custom field in Workiom. |

### Lists

| Action | Method | Description |
| --- | --- | --- |
| [Create List](actions/create-list.md) | POST | Creates a new list in your Workiom workspace. |
| [Get List](actions/get-list.md) | GET | Retrieves a list from your Workiom workspace. |
| [List Lists](actions/list-lists.md) | GET | Retrieves lists from your Workiom workspace. |
| [Update List](actions/update-list.md) | PUT | Updates an existing list in your Workiom workspace. |

### Records

| Action | Method | Description |
| --- | --- | --- |
| [Create Record](actions/create-record.md) | POST | Creates a new record in your Workiom workspace. |
| [Delete Record](actions/delete-record.md) | DELETE | Deletes an existing record from your Workiom workspace. |
| [Get App Records Count](actions/get-app-records-count.md) | GET | Retrieves an app's record count from Workiom. |
| [Get Record](actions/get-record.md) | GET | Retrieves a record from your Workiom workspace. |
| [Get Summary](actions/get-summary.md) | GET | Retrieves record summary data from your Workiom workspace. |
| [List Records](actions/list-records.md) | GET | Retrieves records from your Workiom workspace. |
| [List Records by Field Value](actions/list-records-by-field-value.md) | GET | Finds records in Workiom by field value. |
| [List Records With Dependency](actions/list-records-with-dependency.md) | GET | Retrieves records with dependency data from Workiom. |
| [Lookup Records](actions/lookup-records.md) | GET | Finds records in Workiom by lookup criteria. |
| [Update Record](actions/update-record.md) | PUT | Updates an existing record in your Workiom workspace. |

### Views

| Action | Method | Description |
| --- | --- | --- |
| [Create View](actions/create-view.md) | POST | Creates a new view in your Workiom workspace. |
| [Get View](actions/get-view.md) | GET | Retrieves a view from your Workiom workspace. |
| [List Views](actions/list-views.md) | GET | Retrieves views from your Workiom workspace. |
| [Update View](actions/update-view.md) | PUT | Updates an existing view in your Workiom workspace. |

