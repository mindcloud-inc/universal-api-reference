# <img src="https://images.mindcloud.co/apps/icons/fillout-icon_1776260648290.png" alt="Fillout logo" width="28" height="28"> Fillout: Universal API

Connect Fillout forms and Zite databases to list forms, manage submissions, and work with databases, tables, fields, and records through the Fillout REST APIs.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/fillout/latest
- **Actions:** 26
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.fillout.com/
- **Vendor API docs:** https://support.fillout.com/help/database/api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Forms](actions/list-forms.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fillout/latest/actions/list-forms?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (26)

### Columns

| Action | Method | Description |
| --- | --- | --- |
| [Create Field](actions/create-field.md) | POST | Creates a new field in Fillout. |
| [Delete Field](actions/delete-field.md) | DELETE | Deletes a field from Fillout. |
| [Update Field](actions/update-field.md) | PUT | Updates a field in Fillout. |

### Databases

| Action | Method | Description |
| --- | --- | --- |
| [Create Database](actions/create-database.md) | POST | Creates a new database in Fillout. |
| [Delete Database](actions/delete-database.md) | DELETE | Deletes a database from Fillout. |
| [Get Database By Id](actions/get-database-by-id.md) | GET | Retrieves a database from Fillout by ID. |
| [Get Databases](actions/get-databases.md) | GET | Retrieves databases from Fillout. |

### Forms

| Action | Method | Description |
| --- | --- | --- |
| [Get Form Metadata](actions/get-form-metadata.md) | GET | Retrieves form metadata from Fillout. |
| [List Forms](actions/list-forms.md) | GET | Retrieves forms from Fillout. |

### Unknown Objects

| Action | Method | Description |
| --- | --- | --- |
| [Create Form Submission](actions/create-form-submission.md) | POST | Creates form submissions in Fillout. |
| [Create Record](actions/create-record.md) | POST | Creates a new record in Fillout. |
| [Create Table](actions/create-table.md) | POST | Creates a new table in Fillout. |
| [Delete Form Submission](actions/delete-form-submission.md) | DELETE | Deletes a form submission from Fillout. |
| [Delete Record](actions/delete-record.md) | DELETE | Deletes a record from Fillout. |
| [Delete Table](actions/delete-table.md) | DELETE | Deletes a table from Fillout. |
| [Get Form Submission](actions/get-form-submission.md) | GET | Retrieves a form submission from Fillout. |
| [Get Record By Id](actions/get-record-by-id.md) | GET | Retrieves a record from Fillout by ID. |
| [List Form Submissions](actions/list-form-submissions.md) | GET | Retrieves form submissions from Fillout. |
| [List Records](actions/list-records.md) | GET | Retrieves records from Fillout. |
| [Update Record](actions/update-record.md) | PUT | Updates a record in Fillout. |
| [Update Table](actions/update-table.md) | PUT | Updates a table in Fillout. |

### Webhook Endpoints

| Action | Method | Description |
| --- | --- | --- |
| [Create Database Webhook](actions/create-database-webhook.md) | POST | Creates a database webhook in Fillout. |
| [Create Form Webhook](actions/create-form-webhook.md) | POST | Creates a form webhook in Fillout. |
| [Delete Database Webhook](actions/delete-database-webhook.md) | DELETE | Deletes a database webhook from Fillout. |
| [Delete Form Webhook](actions/delete-form-webhook.md) | DELETE | Deletes a form webhook from Fillout. |
| [List Database Webhooks](actions/list-database-webhooks.md) | GET | Retrieves database webhooks from Fillout. |

