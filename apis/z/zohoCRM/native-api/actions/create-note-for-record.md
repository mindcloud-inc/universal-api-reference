# Create Note for Record with Zoho CRM

Creates a new note for a Zoho CRM record.

## Endpoint

- **Method:** `POST`
- **Path:** `/Notes`
- **Base URL:** `{api_domain}/crm/v8`
- **Official documentation:** [Create Note for Record](https://www.zoho.com/crm/developer/docs/api/v8/create-notes.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data[].Parent_Id.id` | body | `string` | yes | Parent record ID for the note. |
| `data[].Parent_Id.module.api_name` | body | `string` | yes | Parent module API name for the note. |
| `data[].Note_Content` | body | `string` | yes | Body content for the note. |
| `data[].Note_Title` | body | `string` | no | Optional title for the note. |
| `data[].$is_shared_to_client` | body | `boolean` | no | Share the note to the client portal. |
