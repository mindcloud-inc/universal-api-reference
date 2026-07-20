# <img src="https://images.mindcloud.co/apps/icons/quinta-db_1774297865418.png" alt="QuintaDB logo" width="28" height="28"> QuintaDB: Universal API

Build forms, manage databases, and automate business workflows

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/quintaDB/latest
- **Category:** IT Operations / Database
- **Actions:** 34
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://quintadb.com
- **Vendor API docs:** https://quintadb.com/api/index

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Databases](actions/list-databases.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quintaDB/latest/actions/list-databases?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (34)

### Action Result

| Action | Method | Description |
| --- | --- | --- |
| [Run Field Action](actions/run-field-action.md) | GET | Runs a field action on a QuintaDB record. |
| [Run Field Actions](actions/run-field-actions.md) | GET | Runs a field action on multiple QuintaDB records. |

### Database

| Action | Method | Description |
| --- | --- | --- |
| [Create Database](actions/create-database.md) | POST | Creates a new database in QuintaDB. |
| [Delete Database](actions/delete-database.md) | DELETE | Deletes an existing database from QuintaDB. |
| [Get Database](actions/get-database.md) | GET | Retrieves a database from QuintaDB by ID. |
| [Get Database By Name](actions/get-database-by-name.md) | GET | Finds a database in QuintaDB by name. |
| [List Databases](actions/list-databases.md) | GET | Retrieves all available databases from QuintaDB. |
| [Update Database](actions/update-database.md) | PUT | Updates an existing database in QuintaDB. |

### Field

| Action | Method | Description |
| --- | --- | --- |
| [Create Field](actions/create-field.md) | POST | Creates a new field in QuintaDB. |
| [Delete Field](actions/delete-field.md) | DELETE | Deletes an existing field from QuintaDB. |
| [Get Field](actions/get-field.md) | GET | Retrieves a field from QuintaDB by ID. |
| [List Fields](actions/list-fields.md) | GET | Retrieves all fields from a QuintaDB form. |
| [Update Field](actions/update-field.md) | PUT | Updates an existing field in QuintaDB. |

### Form

| Action | Method | Description |
| --- | --- | --- |
| [Create Form](actions/create-form.md) | POST | Creates a new form in QuintaDB. |
| [Delete Form](actions/delete-form.md) | DELETE | Deletes an existing form from QuintaDB. |
| [Get Form](actions/get-form.md) | GET | Retrieves a form from QuintaDB by ID. |
| [Get Form By Name](actions/get-form-by-name.md) | GET | Finds a form in QuintaDB by name. |
| [List Forms](actions/list-forms.md) | GET | Retrieves all forms from a QuintaDB database. |
| [Update Form](actions/update-form.md) | PUT | Updates an existing form in QuintaDB. |

### Other

| Action | Method | Description |
| --- | --- | --- |
| [Get Field Total](actions/get-field-total.md) | GET | Retrieves a total for a QuintaDB field. |
| [Get Relation Field ID](actions/get-relation-field-id.md) | GET | Retrieves a relation field ID from QuintaDB. |
| [Remove File](actions/remove-file.md) | PUT | Removes a file from a QuintaDB record. |

### Record

| Action | Method | Description |
| --- | --- | --- |
| [Create Record](actions/create-record.md) | POST | Creates a new record in QuintaDB. |
| [Delete All Records](actions/delete-all-records.md) | DELETE | Deletes all records from a QuintaDB form. |
| [Delete Many Records](actions/delete-many-records.md) | DELETE | Deletes multiple selected records from QuintaDB. |
| [Delete Record](actions/delete-record.md) | DELETE | Deletes an existing record from QuintaDB. |
| [Get Record](actions/get-record.md) | GET | Retrieves a record from QuintaDB by ID. |
| [List Records](actions/list-records.md) | GET | Retrieves records from a QuintaDB form. |
| [Search Records](actions/search-records.md) | GET | Finds records in QuintaDB by search criteria. |
| [Update All Records](actions/update-all-records.md) | PUT | Updates all records in a QuintaDB form. |
| [Update Cell Value](actions/update-cell-value.md) | PUT | Updates a single cell value in QuintaDB. |
| [Update Many Records](actions/update-many-records.md) | PUT | Updates multiple selected records in QuintaDB. |
| [Update Record](actions/update-record.md) | PUT | Updates an existing record in QuintaDB. |

### Report

| Action | Method | Description |
| --- | --- | --- |
| [List Reports](actions/list-reports.md) | GET | Retrieves reports from a QuintaDB form. |

