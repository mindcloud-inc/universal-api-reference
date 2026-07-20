# <img src="https://images.mindcloud.co/apps/icons/quickbase-icon_1782394265009.png" alt="Quickbase logo" width="28" height="28"> Quickbase: Universal API

Manage Quickbase apps, tables, fields, and records

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/quickbase/latest
- **Category:** IT Operations / Database
- **Actions:** 20
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.quickbase.com/
- **Vendor API docs:** https://developer.quickbase.com/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get App](actions/get-app.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quickbase/latest/actions/get-app?connectionId=$CONNECTION_ID&appId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (20)

### Applications

| Action | Method | Description |
| --- | --- | --- |
| [Get App](actions/get-app.md) | GET | Retrieves a Quickbase app by ID. |

### Custom Fields

| Action | Method | Description |
| --- | --- | --- |
| [Create a Field](actions/create-a-field.md) | POST | Creates a new field in Quickbase. |
| [Delete Field(s)](actions/delete-fields.md) | DELETE | Deletes existing fields from a Quickbase table. |
| [Get Field](actions/get-field.md) | GET | Retrieves a Quickbase field by ID. |
| [Get Fields for a Table](actions/get-fields-for-a-table.md) | GET | Retrieves all fields in a Quickbase table. |
| [Update a Field](actions/update-a-field.md) | PUT | Updates an existing field in Quickbase. |

### Custom Objects

| Action | Method | Description |
| --- | --- | --- |
| [Create a Table](actions/create-a-table.md) | POST | Creates a new table in Quickbase. |
| [Delete a Table](actions/delete-a-table.md) | DELETE | Deletes an existing table from Quickbase. |
| [Delete Record(s)](actions/delete-records.md) | DELETE | Deletes records from a Quickbase table. |
| [Get a Table](actions/get-a-table.md) | GET | Retrieves a Quickbase table by ID. |
| [Get Records Modified Since](actions/get-records-modified-since.md) | GET | Retrieves Quickbase records modified after a specified timestamp. |
| [Get Tables for an App](actions/get-tables-for-an-app.md) | GET | Retrieves all tables in a Quickbase app. |
| [Insert/Update Record(s)](actions/insert-update-records.md) | POST | Creates Quickbase records, or updates matching records if they exist. |
| [Query for Data](actions/query-for-data.md) | GET | Queries records from a Quickbase table. |
| [Update a Table](actions/update-a-table.md) | PUT | Updates an existing table in Quickbase. |

### Queries

| Action | Method | Description |
| --- | --- | --- |
| [Run a Formula](actions/run-a-formula.md) | GET | Evaluates a Quickbase formula and returns the result. |

### Reports

| Action | Method | Description |
| --- | --- | --- |
| [Get a Report](actions/get-a-report.md) | GET | Retrieves a Quickbase report by ID. |
| [Get Reports for a Table](actions/get-reports-for-a-table.md) | GET | Retrieves all reports for a Quickbase table. |
| [Run a Report](actions/run-a-report.md) | GET | Runs a Quickbase report and returns its results. |

### Roles

| Action | Method | Description |
| --- | --- | --- |
| [Get Roles](actions/get-roles.md) | GET | Retrieves all roles in a Quickbase app. |

