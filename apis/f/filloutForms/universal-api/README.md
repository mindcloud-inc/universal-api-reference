# <img src="https://images.mindcloud.co/apps/icons/fillout-forms_1772806492562.png" alt="Fillout Forms logo" width="28" height="28"> Fillout Forms: Universal API

Build forms, collect responses, automate workflows, and analyze results.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/filloutForms/latest
- **Category:** Productivity / Forms & Surveys
- **Actions:** 26
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.fillout.com
- **Vendor API docs:** https://www.fillout.com/help/fillout-rest-api

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Forms](actions/list-forms.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/filloutForms/latest/actions/list-forms?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (26)

### Database

| Action | Method | Description |
| --- | --- | --- |
| [Create Database](actions/create-database.md) | POST | Creates a database in Fillout. |
| [Delete Database](actions/delete-database.md) | DELETE | Deletes a database from Fillout. |
| [Get Database by ID](actions/get-database-by-id.md) | GET | Retrieves a database by ID from Fillout. |
| [List Databases](actions/list-databases.md) | GET | Retrieves databases from Fillout. |

### Database Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Database Webhook](actions/create-database-webhook.md) | POST | Creates a database webhook in Fillout. |
| [Delete Database Webhook](actions/delete-database-webhook.md) | DELETE | Deletes a database webhook from Fillout. |
| [List Database Webhooks](actions/list-database-webhooks.md) | GET | Retrieves database webhooks from Fillout. |

### Field

| Action | Method | Description |
| --- | --- | --- |
| [Create Field](actions/create-field.md) | POST | Creates a field in Fillout. |
| [Delete Field](actions/delete-field.md) | DELETE | Deletes a field from Fillout. |
| [Update Field](actions/update-field.md) | PUT | Updates an existing field in Fillout. |

### Form

| Action | Method | Description |
| --- | --- | --- |
| [Get Form Metadata](actions/get-form-metadata.md) | GET | Retrieves metadata for a Fillout form. |
| [List Forms](actions/list-forms.md) | GET | Retrieves forms from Fillout. |

### Record

| Action | Method | Description |
| --- | --- | --- |
| [Create Record](actions/create-record.md) | POST | Creates a record in Fillout. |
| [Delete Record](actions/delete-record.md) | DELETE | Deletes a record from Fillout. |
| [Get Record by ID](actions/get-record-by-id.md) | GET | Retrieves a record by ID from Fillout. |
| [List Records](actions/list-records.md) | GET | Retrieves records from a Fillout table. |
| [Update Record](actions/update-record.md) | PUT | Updates an existing record in Fillout. |

### Submission

| Action | Method | Description |
| --- | --- | --- |
| [Create Submissions](actions/create-submissions.md) | POST | Creates submissions for a Fillout form. |
| [Delete Submission by ID](actions/delete-submission-by-id.md) | DELETE | Deletes a submission by ID from Fillout. |
| [Get Submission by ID](actions/get-submission-by-id.md) | GET | Retrieves a submission by ID from Fillout. |
| [List Submissions](actions/list-submissions.md) | GET | Retrieves submissions for a Fillout form. |

### Table

| Action | Method | Description |
| --- | --- | --- |
| [Create Table](actions/create-table.md) | POST | Creates a table in Fillout. |
| [Delete Table](actions/delete-table.md) | DELETE | Deletes a table from Fillout. |
| [Update Table](actions/update-table.md) | PUT | Updates an existing table in Fillout. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a webhook in Fillout. |
| [Remove Webhook](actions/remove-webhook.md) | DELETE | Deletes a webhook from Fillout. |

