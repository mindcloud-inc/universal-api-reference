# <img src="https://images.mindcloud.co/apps/icons/smart-suite_1773684321216.png" alt="SmartSuite logo" width="28" height="28"> SmartSuite: Universal API

Manage workflows, records, and business operations in SmartSuite

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/smartSuite/latest
- **Category:** Productivity / Project Management
- **Actions:** 28
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.smartsuite.com
- **Vendor API docs:** https://developers.smartsuite.com/docs/intro

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [List Solutions](actions/list-solutions.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartSuite/latest/actions/list-solutions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (28)

### Comment

| Action | Method | Description |
| --- | --- | --- |
| [Add Comment](actions/add-comment.md) | POST | Creates a new comment in SmartSuite. |
| [List Comments](actions/list-comments.md) | GET | Retrieves comments from SmartSuite. |

### Field

| Action | Method | Description |
| --- | --- | --- |
| [Add Field](actions/add-field.md) | POST | Creates a new field in SmartSuite. |
| [Delete Field](actions/delete-field.md) | DELETE | Deletes an existing field from SmartSuite. |
| [Update Field](actions/update-field.md) | PUT | Updates an existing field in SmartSuite. |

### File

| Action | Method | Description |
| --- | --- | --- |
| [Get File URL](actions/get-file-url.md) | GET | Retrieves a shared file URL from SmartSuite. |

### Record

| Action | Method | Description |
| --- | --- | --- |
| [Attach File](actions/attach-file.md) | PUT | Attaches a file to a SmartSuite record. |
| [Bulk Add Records](actions/bulk-add-records.md) | POST | Creates multiple records in SmartSuite. |
| [Bulk Delete Records](actions/bulk-delete-records.md) | DELETE | Deletes existing records from SmartSuite in bulk. |
| [Bulk Update Records](actions/bulk-update-records.md) | PUT | Updates existing records in SmartSuite in bulk. |
| [Create Record](actions/create-record.md) | POST | Creates a new record in SmartSuite. |
| [Delete Record](actions/delete-record.md) | DELETE | Deletes an existing record from SmartSuite. |
| [Get Record](actions/get-record.md) | GET | Retrieves a record from SmartSuite. |
| [Get Records For View](actions/get-records-for-view.md) | GET | Retrieves records for a SmartSuite view. |
| [List Deleted Records](actions/list-deleted-records.md) | GET | Retrieves deleted records from SmartSuite. |
| [Restore Deleted Record](actions/restore-deleted-record.md) | PUT | Restores a deleted record in SmartSuite. |
| [Update Record](actions/update-record.md) | PUT | Updates an existing record in SmartSuite. |

### Solution

| Action | Method | Description |
| --- | --- | --- |
| [Create Solution](actions/create-solution.md) | POST | Creates a new solution in SmartSuite. |
| [Duplicate Solution](actions/duplicate-solution.md) | POST | Creates a duplicate of a solution in SmartSuite. |
| [Get Solution](actions/get-solution.md) | GET | Retrieves a solution from SmartSuite. |
| [List Solutions](actions/list-solutions.md) | GET | Retrieves solutions from SmartSuite. |

### Table

| Action | Method | Description |
| --- | --- | --- |
| [Create Table](actions/create-table.md) | POST | Creates a new table in SmartSuite. |
| [Get Table](actions/get-table.md) | GET | Retrieves a table from SmartSuite. |
| [List Tables](actions/list-tables.md) | GET | Retrieves tables from SmartSuite. |

### View

| Action | Method | Description |
| --- | --- | --- |
| [Create View](actions/create-view.md) | POST | Creates a new view in SmartSuite. |

### Webhook

| Action | Method | Description |
| --- | --- | --- |
| [Create Webhook](actions/create-webhook.md) | POST | Creates a new webhook in SmartSuite. |
| [Get Webhook](actions/get-webhook.md) | GET | Retrieves a webhook from SmartSuite. |
| [List Webhooks](actions/list-webhooks.md) | GET | Retrieves webhooks from SmartSuite. |

