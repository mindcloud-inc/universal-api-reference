# Convert Lead with Zoho CRM

Converts a lead into CRM records in Zoho CRM.

## Endpoint

- **Method:** `POST`
- **Path:** `/Leads/:record_id/actions/convert`
- **Base URL:** `{api_domain}/crm/v8`
- **Official documentation:** [Convert Lead](https://www.zoho.com/crm/developer/docs/api/v8/convert-lead.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `record_id` | path | `string` | yes | Lead record ID to convert. |
| `data[].overwrite` | body | `boolean` | no | Overwrite existing mapped values during conversion. |
| `data[].notify_lead_owner` | body | `boolean` | no | Notify the lead owner about the conversion. |
| `data[].notify_new_entity_owner` | body | `boolean` | no | Notify the owner of the newly created record. |
| `data[].move_attachments_to.api_name` | body | `list` | no | Module that should receive converted lead attachments. Accepted values: `Accounts`, `Contacts`, `Deals`. |
| `data[].assign_to.id` | body | `string` | no | User ID for the converted record owner. |
| `data[].Accounts.id` | body | `string` | no | Existing account ID to associate during conversion. |
| `data[].Contacts.id` | body | `string` | no | Existing contact ID to associate during conversion. |
