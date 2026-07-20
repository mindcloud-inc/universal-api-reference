# <img src="https://images.mindcloud.co/apps/icons/baserow_1773759899121.png" alt="Baserow logo" width="28" height="28"> Baserow: Universal API

Manage Baserow databases, tables, and rows

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/baserow/latest
- **Category:** IT Operations / Database
- **Actions:** 17
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://baserow.io
- **Vendor API docs:** https://api.baserow.io/api/redoc/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List All Tables](actions/list-all-tables.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/baserow/latest/actions/list-all-tables?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (17)

### Authentication

| Action | Method | Description |
| --- | --- | --- |
| [Password Field Authentication](actions/password-field-authentication.md) | GET | Checks a Baserow row against a password field. |

### Database Token

| Action | Method | Description |
| --- | --- | --- |
| [Check Database Token](actions/check-database-token.md) | GET | Checks whether a Baserow API token is valid. |

### Field

| Action | Method | Description |
| --- | --- | --- |
| [Create Field](actions/create-field.md) | POST | Creates a new field in Baserow. |
| [List Fields](actions/list-fields.md) | GET | Retrieves fields from a Baserow table. |

### File

| Action | Method | Description |
| --- | --- | --- |
| [Upload File](actions/upload-file.md) | POST | Uploads a file directly to Baserow. |
| [Upload File Via URL](actions/upload-file-via-url.md) | POST | Uploads a file to Baserow from a URL. |

### Row

| Action | Method | Description |
| --- | --- | --- |
| [Batch Create Rows](actions/batch-create-rows.md) | POST | Creates multiple rows in a Baserow table. |
| [Batch Delete Rows](actions/batch-delete-rows.md) | DELETE | Deletes multiple rows from a Baserow table. |
| [Batch Update Rows](actions/batch-update-rows.md) | PUT | Updates multiple rows in a Baserow table. |
| [Create Row](actions/create-row.md) | POST | Creates a new row in Baserow. |
| [Delete Row](actions/delete-row.md) | DELETE | Deletes an existing row from Baserow. |
| [Get Row](actions/get-row.md) | GET | Retrieves a row from Baserow. |
| [List Row Names](actions/list-row-names.md) | GET | Retrieves primary row names from Baserow. |
| [List Rows](actions/list-rows.md) | GET | Retrieves rows from a Baserow table. |
| [Move Row](actions/move-row.md) | PUT | Moves an existing row in a Baserow table. |
| [Update Row](actions/update-row.md) | PUT | Updates an existing row in Baserow. |

### Table

| Action | Method | Description |
| --- | --- | --- |
| [List All Tables](actions/list-all-tables.md) | GET | Retrieves all accessible tables from Baserow. |

