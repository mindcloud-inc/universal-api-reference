# <img src="https://images.mindcloud.co/apps/icons/gridfox_1775164864803.png" alt="Gridfox logo" width="28" height="28"> Gridfox: Universal API

Gridfox is a work management platform for replacing spreadsheets with custom tables, records, and project workflows.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/gridfox/latest
- **Category:** Productivity / Project Management
- **Actions:** 15
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://gridfox.com
- **Vendor API docs:** https://api.gridfox.com/swagger/index.html

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Tables](actions/list-tables.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gridfox/latest/actions/list-tables?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (15)

### Audit Log

| Action | Method | Description |
| --- | --- | --- |
| [List Record Audits](actions/list-record-audits.md) | GET | Retrieves audit entries for a Gridfox record. |

### File

| Action | Method | Description |
| --- | --- | --- |
| [Delete Field File](actions/delete-field-file.md) | DELETE | Deletes a file from a Gridfox record field. |
| [Download Field File](actions/download-field-file.md) | GET | Downloads a file from a Gridfox record field. |
| [Upload Field Files](actions/upload-field-files.md) | PUT | Adds files to a file field in Gridfox. |

### Group

| Action | Method | Description |
| --- | --- | --- |
| [Search User Groups](actions/search-user-groups.md) | GET | Finds user groups in a Gridfox project. |

### Permission

| Action | Method | Description |
| --- | --- | --- |
| [Get Permissions](actions/get-permissions.md) | GET | Retrieves a user's project permissions from Gridfox. |

### Record

| Action | Method | Description |
| --- | --- | --- |
| [Create Record](actions/create-record.md) | POST | Creates a new record in a Gridfox table. |
| [Delete Record](actions/delete-record.md) | DELETE | Deletes an existing record from a Gridfox table. |
| [Get Record](actions/get-record.md) | GET | Retrieves a record from a Gridfox table. |
| [Search Records](actions/search-records.md) | GET | Finds records in a Gridfox table. |
| [Update Record](actions/update-record.md) | PUT | Updates an existing record in a Gridfox table. |

### Table

| Action | Method | Description |
| --- | --- | --- |
| [List Tables](actions/list-tables.md) | GET | Retrieves tables in a Gridfox project. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Add User](actions/add-user.md) | POST | Adds a user to a Gridfox project. |
| [Remove User](actions/remove-user.md) | DELETE | Removes a user from a Gridfox project. |
| [Update User Group](actions/update-user-group.md) | PUT | Updates a user's group in a Gridfox project. |

