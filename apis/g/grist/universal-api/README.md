# <img src="https://images.mindcloud.co/apps/icons/grist_1771963451648.png" alt="Grist logo" width="28" height="28"> Grist: Universal API

Connect to Grist to read, create, and update tables, records, and metadata so you can automate spreadsheet-database workflows across your tools.

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/grist/latest
- **Category:** IT Operations / Database
- **Actions:** 24
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor API docs:** https://support.getgrist.com/api/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Document](actions/get-document.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/grist/latest/actions/get-document?connectionId=$CONNECTION_ID&docId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (24)

### Column

| Action | Method | Description |
| --- | --- | --- |
| [Add Columns](actions/add-columns.md) | POST | Creates new columns in a Grist table. |
| [Delete Column](actions/delete-column.md) | DELETE | Deletes a column from a Grist table. |
| [List Columns](actions/list-columns.md) | GET | Finds columns in a Grist table. |
| [Replace Columns](actions/replace-columns.md) | PUT | Replaces columns in a Grist table. |

### Document

| Action | Method | Description |
| --- | --- | --- |
| [Create Document](actions/create-document.md) | POST | Creates a new document in Grist. |
| [Delete Document](actions/delete-document.md) | DELETE | Deletes a document from Grist. |
| [Get Document](actions/get-document.md) | GET | Retrieves a document from Grist. |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization](actions/get-organization.md) | GET | Retrieves an organization from Grist. |
| [List Organizations](actions/list-organizations.md) | GET | Finds organizations in Grist. |

### Record

| Action | Method | Description |
| --- | --- | --- |
| [Add Records](actions/add-records.md) | POST | Creates new records in a Grist table. |
| [Delete Records](actions/delete-records.md) | DELETE | Deletes records from a Grist table. |
| [List Records](actions/list-records.md) | GET | Finds records in a Grist table. |
| [Replace Records](actions/replace-records.md) | PUT | Replaces records in a Grist table. |
| [Update Records](actions/update-records.md) | PUT | Updates existing records in a Grist table. |

### Sql

| Action | Method | Description |
| --- | --- | --- |
| [Run SQL Query](actions/run-sql-query.md) | GET | Runs a SQL query in a Grist document. |

### Table

| Action | Method | Description |
| --- | --- | --- |
| [Add Tables](actions/add-tables.md) | POST | Creates new tables in a Grist document. |
| [List Tables](actions/list-tables.md) | GET | Finds tables in a Grist document. |
| [Update Tables](actions/update-tables.md) | PUT | Updates existing tables in a Grist document. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in a Grist document. |
| [Delete Webhook](actions/delete-webhook.md) | DELETE | Deletes a webhook from a Grist document. |
| [List Webhooks](actions/list-webhooks.md) | GET | Finds webhooks in a Grist document. |
| [Update Webhook](actions/update-webhook.md) | PUT | Updates an existing webhook in a Grist document. |

### Workspace

| Action | Method | Description |
| --- | --- | --- |
| [Get Workspace](actions/get-workspace.md) | GET | Retrieves a workspace from Grist. |
| [List Workspaces](actions/list-workspaces.md) | GET | Finds workspaces in a Grist organization. |

