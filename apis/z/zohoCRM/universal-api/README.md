# <img src="https://images.mindcloud.co/apps/icons/zoho-crm_1782741849165.png" alt="Zoho CRM logo" width="28" height="28"> Zoho CRM: Universal API

Manage leads, contacts, deals, and sales activities

- **Interactive docs:** https://mindcloud.co/docs/universal/rest/zohoCRM/latest
- **Category:** Sales & CRM / CRM
- **Actions:** 38
- **OpenAPI specification:** [openapi.json](openapi.json)
- **Vendor website:** https://www.zoho.com/crm/
- **Vendor API docs:** https://www.zoho.com/crm/developer/docs/api/v8/

## Quickstart

Every action below is called through one REST interface, authenticated with a MindCloud API key and a `connectionId`.

Read more in [authentication.md](authentication.md).

For example, to [Get Account](actions/get-account.md):

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoCRM/latest/actions/get-account?connectionId=$CONNECTION_ID&ids=string&fields=id%2CAccount_Name%2CPhone%2CWebsite" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

## Actions (38)

### Account

| Action | Method | Description |
| --- | --- | --- |
| [Create Account](actions/create-account.md) | POST | Creates a new account in Zoho CRM. |
| [Search Accounts](actions/search-accounts.md) | GET | Finds account records in Zoho CRM by search criteria. |
| [Update Account](actions/update-account.md) | PUT | Updates an existing account in Zoho CRM. |
| [Upsert Account](actions/upsert-account.md) | POST | Finds an account in Zoho CRM, or creates one if needed. |

### Companies

| Action | Method | Description |
| --- | --- | --- |
| [Get Account](actions/get-account.md) | GET | Retrieves an account record from Zoho CRM. |
| [List Accounts](actions/list-accounts.md) | GET | Retrieves account records from Zoho CRM. |

### Contact

| Action | Method | Description |
| --- | --- | --- |
| [Create Contact](actions/create-contact.md) | POST | Creates a new contact in Zoho CRM. |
| [Get Contact](actions/get-contact.md) | GET | Retrieves a contact record from Zoho CRM. |
| [List Contacts](actions/list-contacts.md) | GET | Retrieves contact records from Zoho CRM. |
| [Search Contacts](actions/search-contacts.md) | GET | Finds contact records in Zoho CRM by search criteria. |
| [Update Contact](actions/update-contact.md) | PUT | Updates an existing contact in Zoho CRM. |
| [Upsert Contact](actions/upsert-contact.md) | POST | Finds a contact in Zoho CRM, or creates one if needed. |

### Coql Result

| Action | Method | Description |
| --- | --- | --- |
| [Get Records through COQL Query](actions/get-records-through-coql-query.md) | GET | Retrieves records from Zoho CRM using a COQL query. |

### Deal

| Action | Method | Description |
| --- | --- | --- |
| [Create Deal](actions/create-deal.md) | POST | Creates a new deal in Zoho CRM. |
| [Get Deal](actions/get-deal.md) | GET | Retrieves a deal record from Zoho CRM. |
| [List Deals](actions/list-deals.md) | GET | Retrieves deal records from Zoho CRM. |
| [Search Deals](actions/search-deals.md) | GET | Finds deal records in Zoho CRM by search criteria. |
| [Update Deal](actions/update-deal.md) | PUT | Updates an existing deal in Zoho CRM. |
| [Upsert Deal](actions/upsert-deal.md) | POST | Finds a deal in Zoho CRM, or creates one if needed. |

### Documents

| Action | Method | Description |
| --- | --- | --- |
| [Get Opportunity Group](actions/get-opportunity-group.md) | GET | Retrieves an Opportunity Group from Zoho CRM. |

### Field Metadata

| Action | Method | Description |
| --- | --- | --- |
| [Get Fields Metadata](actions/get-fields-metadata.md) | GET | Retrieves field metadata for a Zoho CRM module. |

### Lead

| Action | Method | Description |
| --- | --- | --- |
| [Convert Lead](actions/convert-lead.md) | PUT | Converts a lead into CRM records in Zoho CRM. |
| [Create Lead](actions/create-lead.md) | POST | Creates a new lead in Zoho CRM. |
| [Get Lead](actions/get-lead.md) | GET | Retrieves a lead record from Zoho CRM. |
| [List Leads](actions/list-leads.md) | GET | Retrieves lead records from Zoho CRM. |
| [Search Leads](actions/search-leads.md) | GET | Finds lead records in Zoho CRM by search criteria. |
| [Update Lead](actions/update-lead.md) | PUT | Updates an existing lead in Zoho CRM. |
| [Upsert Lead](actions/upsert-lead.md) | POST | Finds a lead in Zoho CRM, or creates one if needed. |

### Module

| Action | Method | Description |
| --- | --- | --- |
| [Get Modules](actions/get-modules.md) | GET | Retrieves available modules from Zoho CRM. |

### Note

| Action | Method | Description |
| --- | --- | --- |
| [Create Note for Record](actions/create-note-for-record.md) | POST | Creates a new note for a Zoho CRM record. |
| [Get Notes for Record](actions/get-notes-for-record.md) | GET | Retrieves notes for a Zoho CRM record. |
| [Update Note](actions/update-note.md) | PUT | Updates an existing note in Zoho CRM. |

### Opportunity Group

| Action | Method | Description |
| --- | --- | --- |
| [Create Opportunity Group](actions/create-opportunity-group.md) | POST | Creates a new Opportunity Group in Zoho CRM. |
| [Search Opportunity Groups](actions/search-opportunity-groups.md) | GET | Finds Opportunity Groups in Zoho CRM by search criteria. |
| [Update Opportunity Group](actions/update-opportunity-group.md) | PUT |  |

### Organization

| Action | Method | Description |
| --- | --- | --- |
| [Get Organization Details](actions/get-organization-details.md) | GET | Retrieves organization details from Zoho CRM. |

### Related Record

| Action | Method | Description |
| --- | --- | --- |
| [Get Related Records](actions/get-related-records.md) | GET | Retrieves related records for a Zoho CRM record. |

### User

| Action | Method | Description |
| --- | --- | --- |
| [Get Users](actions/get-users.md) | GET | Retrieves user records from Zoho CRM. |

