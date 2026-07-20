# <img src="https://images.mindcloud.co/apps/icons/bigin-256_1775165753307.png" alt="Bigin by Zoho CRM logo" width="28" height="28"> Bigin by Zoho CRM: Universal API

Manage contacts, companies, deals, notes, and activities

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/biginByZohoCRM/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 22
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.bigin.com/
- **Vendor API docs:** https://www.bigin.com/developer/docs/apis/v2/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Count Records](actions/count-records.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/biginByZohoCRM/latest/actions/count-records?connectionId=$CONNECTION_ID&moduleApiName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (22)

### Attachment

| Action | Method | Description |
| --- | --- | --- |
| [List Record Attachments](actions/list-record-attachments.md) | GET | Retrieves attachments for a record in Bigin by Zoho CRM. |

### Deleted Record

| Action | Method | Description |
| --- | --- | --- |
| [List Deleted Records](actions/list-deleted-records.md) | GET | Retrieves deleted records from a Bigin by Zoho CRM module. |

### Field

| Action | Method | Description |
| --- | --- | --- |
| [List Fields](actions/list-fields.md) | GET | Retrieves field metadata from a Bigin by Zoho CRM module. |

### Module

| Action | Method | Description |
| --- | --- | --- |
| [List Modules](actions/list-modules.md) | GET | Retrieves module details from Bigin by Zoho CRM. |

### Note

| Action | Method | Description |
| --- | --- | --- |
| [Add Notes](actions/add-notes.md) | POST | Creates standalone notes in Bigin by Zoho CRM. |
| [Add Record Notes](actions/add-record-notes.md) | POST | Creates notes for a record in Bigin by Zoho CRM. |
| [List Notes](actions/list-notes.md) | GET | Retrieves notes from Bigin by Zoho CRM. |
| [List Record Notes](actions/list-record-notes.md) | GET | Retrieves notes for a record in Bigin by Zoho CRM. |

### Record

| Action | Method | Description |
| --- | --- | --- |
| [Add Records](actions/add-records.md) | POST | Creates new records in a Bigin by Zoho CRM module. |
| [Delete Record](actions/delete-record.md) | DELETE | Deletes an existing record from a Bigin by Zoho CRM module. |
| [Delete Records](actions/delete-records.md) | DELETE | Deletes existing records from a Bigin by Zoho CRM module. |
| [Get Record](actions/get-record.md) | GET | Retrieves a record from a Bigin by Zoho CRM module. |
| [List Records](actions/list-records.md) | GET | Retrieves records from a Bigin by Zoho CRM module. |
| [Run COQL Query](actions/run-coql-query.md) | GET | Runs a COQL query in Bigin by Zoho CRM. |
| [Search Records](actions/search-records.md) | GET | Finds records in Bigin by Zoho CRM by criteria, email, phone, or word. |
| [Update Record](actions/update-record.md) | PUT | Updates an existing record in a Bigin by Zoho CRM module. |
| [Update Records](actions/update-records.md) | PUT | Updates existing records in a Bigin by Zoho CRM module. |
| [Upsert Records](actions/upsert-records.md) | POST | Creates or updates records in a Bigin by Zoho CRM module. |

### Record Count

| Action | Method | Description |
| --- | --- | --- |
| [Count Records](actions/count-records.md) | GET | Counts records in a Bigin by Zoho CRM module. |

### Related Record

| Action | Method | Description |
| --- | --- | --- |
| [List Related Records](actions/list-related-records.md) | GET | Retrieves related records for a Bigin by Zoho CRM record. |
| [Update Related Records](actions/update-related-records.md) | PUT | Updates related records for a Bigin by Zoho CRM record. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [List Users](actions/list-users.md) | GET | Retrieves users from Bigin by Zoho CRM. |

