# QuintaDB: Native API Reference

A consolidated summary of QuintaDB's API configuration and 34 documented operations, with links to official documentation.

- **Official docs:** https://quintadb.com/api/index
- **API base URL:** `https://quintadb.com`

## Authentication

### REST API key

Use a QuintaDB REST API key to authenticate REST API requests.

### Credentials

- **API Key:** `apiKey` · required

Send these headers with each API request:

```http
Authorization: Bearer <apiKey>
```

[Official authentication documentation](https://quintadb.com/api/index)

## API conventions

Request bodies use JSON.

Shared headers:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

Responses from this API use JSON.

## Pagination

Use `page` in the query string to choose the page; numbering starts at 1.

## Endpoints (34 documented)

| Operation | Method & path | Vendor docs |
| --- | --- | --- |
| [Create Database](actions/create-database.md) | `POST /apps.json` | [docs](https://quintadb.com/api/index#create_database) |
| [Create Field](actions/create-field.md) | `POST /apps/:app_id/entities/:entity_id/properties.json` | [docs](https://quintadb.com/api/index#create_field) |
| [Create Form](actions/create-form.md) | `POST /apps/:app_id/entities.json` | [docs](https://quintadb.com/api/index#create_form) |
| [Create Record](actions/create-record.md) | `POST /apps/:app_id/dtypes.json` | [docs](https://quintadb.com/api/index#create_record) |
| [Delete All Records](actions/delete-all-records.md) | `DELETE /dtypes/:app_id/delete_all/:entity_id.json` | [docs](https://quintadb.com/api/index#delete_all) |
| [Delete Database](actions/delete-database.md) | `DELETE /apps/:app_id.json` | [docs](https://quintadb.com/api/index#delete_database) |
| [Delete Field](actions/delete-field.md) | `DELETE /apps/:app_id/entities/:entity_id/properties/:property_id.json` | [docs](https://quintadb.com/api/index#delete_field) |
| [Delete Form](actions/delete-form.md) | `DELETE /apps/:app_id/entities/:entity_id.json` | [docs](https://quintadb.com/api/index#delete_form) |
| [Delete Many Records](actions/delete-many-records.md) | `POST /apps/:app_id/dtypes/delete_multiple.json` | [docs](https://quintadb.com/api/index#delete_multiple) |
| [Delete Record](actions/delete-record.md) | `DELETE /apps/:app_id/dtypes/:dtype_id.json` | [docs](https://quintadb.com/api/index#delete_record) |
| [Get Database](actions/get-database.md) | `GET /apps/:app_id.json` | [docs](https://quintadb.com/api/index#get_database) |
| [Get Database By Name](actions/get-database-by-name.md) | `GET /apps/search.json` | [docs](https://quintadb.com/api/index#get_database_by_name) |
| [Get Field](actions/get-field.md) | `GET /apps/:app_id/entities/:entity_id/properties/:property_id.json` | [docs](https://quintadb.com/api/index#get_field) |
| [Get Field Total](actions/get-field-total.md) | `GET /search/sum/:entity_id/:property_id.json` | [docs](https://quintadb.com/api/index#get_total_by_column) |
| [Get Form](actions/get-form.md) | `GET /apps/:app_id/entities/:entity_id.json` | [docs](https://quintadb.com/api/index#get_form) |
| [Get Form By Name](actions/get-form-by-name.md) | `GET /apps/search/entities/search.json` | [docs](https://quintadb.com/api/index#get_form_by_name) |
| [Get Record](actions/get-record.md) | `GET /apps/:app_id/dtypes/:dtype_id.json` | [docs](https://quintadb.com/api/index#get_record) |
| [Get Relation Field ID](actions/get-relation-field-id.md) | `GET /entities/:entity_id/get_rel_id/:property_id.json` | [docs](https://quintadb.com/api/index#rels) |
| [List Databases](actions/list-databases.md) | `GET /apps.json` | [docs](https://quintadb.com/api/index#get_databases) |
| [List Fields](actions/list-fields.md) | `GET /apps/:app_id/entities/:entity_id/properties.json` | [docs](https://quintadb.com/api/index#get_fields) |
| [List Forms](actions/list-forms.md) | `GET /apps/:app_id/entities.json` | [docs](https://quintadb.com/api/index#get_forms) |
| [List Records](actions/list-records.md) | `GET /apps/:app_id/dtypes/entity/:entity_id.json` | [docs](https://quintadb.com/api/index#get_records) |
| [List Reports](actions/list-reports.md) | `GET /apps/:app_id/entities/:entity_id/views/index.json` | [docs](https://quintadb.com/api/index#get_reports) |
| [Remove File](actions/remove-file.md) | `GET /dtypes/delete_dtype_file/:app_id/:dtype_id/:property_id.json` | [docs](https://quintadb.com/api/index#remove_files) |
| [Run Field Action](actions/run-field-action.md) | `GET /actions/:action_property_id.json` | [docs](https://quintadb.com/api/index#action) |
| [Run Field Actions](actions/run-field-actions.md) | `GET /actions/:action_property_id.json` | [docs](https://quintadb.com/api/index) |
| [Search Records](actions/search-records.md) | `POST /search/:app_id.json` | [docs](https://quintadb.com/api/index#search) |
| [Update All Records](actions/update-all-records.md) | `POST /dtypes/confirm_action/:app_id/:entity_id.json` | [docs](https://quintadb.com/api/index#update_multiple_all_records) |
| [Update Cell Value](actions/update-cell-value.md) | `PATCH /cell_values/:dtype_id/update_cell_value/:property_id.json` | [docs](https://quintadb.com/api/index#update_cell) |
| [Update Database](actions/update-database.md) | `PUT /apps/:app_id.json` | [docs](https://quintadb.com/api/index#update_database) |
| [Update Field](actions/update-field.md) | `PUT /apps/:app_id/entities/:entity_id/properties/:property_id.json` | [docs](https://quintadb.com/api/index#update_field) |
| [Update Form](actions/update-form.md) | `PUT /apps/:app_id/entities/:entity_id.json` | [docs](https://quintadb.com/api/index#update_form) |
| [Update Many Records](actions/update-many-records.md) | `POST /dtypes/confirm_action/:app_id/:entity_id.json` | [docs](https://quintadb.com/api/index#update_multiple_records) |
| [Update Record](actions/update-record.md) | `PUT /apps/:app_id/dtypes/:dtype_id.json` | [docs](https://quintadb.com/api/index#update_record) |
