# Update Note with Zoho CRM

Updates an existing note in Zoho CRM.

## Endpoint

- **Method:** `PUT`
- **Path:** `/Notes/:note_id`
- **Base URL:** `{api_domain}/crm/v8`
- **Official documentation:** [Update Note](https://www.zoho.com/crm/developer/docs/api/v8/update-notes.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `note_id` | path | `string` | yes | Existing note ID. |
| `data[].Note_Content` | body | `string` | no | Updated note content. |
| `data[].Note_Title` | body | `string` | no | Updated note title. |
| `data[].$is_shared_to_client` | body | `boolean` | no | Updated client-sharing setting. |
