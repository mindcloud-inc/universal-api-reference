# Update Request with Content Snare

Updates a request in Content Snare.

## Endpoint

- **Method:** `PUT`
- **Path:** `/partner_api/v1/requests/{id}`
- **Base URL:** `https://api.contentsnare.com`
- **Official documentation:** [Update Request](https://api.contentsnare.com/partner_api/v1/documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Request ID. |
| `client_assignments_ids[]` | body | `array<object>` | no | Client Assignments Ids. |
| `client_assignments_ids[].account_id` | body | `string` | no | Client id |
| `client_assignments_ids[].client_company_id` | body | `string` | no | Client company id |
| `client_assignments_ids[].primary` | body | `boolean` | no | Set true to mark client as primary. Only one client in request can be primary. |
| `comments_enabled` | body | `boolean` | no | Enable client comments. This allows your client to ask questions about each field. |
| `communication_template_id` | body | `string` | no | Id of communications schedule. Set this parameter as null to remove existing communications schedule from request. |
| `communication_template_name` | body | `string` | no | Name of communications schedule. Set this parameter as null or "None" to remove existing communications schedule from request. |
| `due` | body | `date` | no | Due date for the request. <br><b>Format:</b> yyyy-mm-dd |
| `folder_id` | body | `string` | no | Folder id. Requests may be grouped in to folders on the requests page. Don't send it if you do not wish to group your Requests. |
| `folder_name` | body | `string` | no | Folder name. Requests may be grouped in to folders on the requests page. Don't send it if you do not wish to group your Requests. |
| `instruction_text` | body | `string` | no | Request instructions are the first thing your client will see when they open the request. Use this area to let them know who you are, what the request is for, and provide some simple instructions on how to use Content Snare. |
| `name` | body | `string` | no | Request name |
| `owner_id` | body | `string` | no | Request owner (team member) id |
| `owner_email` | body | `string` | no | Request owner (team member) email |
| `passcode_enabled` | body | `boolean` | no | Protect share with a pin code. Your client will be asked to set their own pincode when they first access the request. |
| `share_via_link_enabled` | body | `boolean` | no | Allow share via link without requiring login |
| `show_instruction` | body | `boolean` | no | Enable request instructions |
| `status` | body | `string` | no | Request status |
| `updated_at` | body | `date` | no | Updated At. |
