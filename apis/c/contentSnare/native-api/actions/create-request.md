# Create Request with Content Snare

Creates a request in Content Snare.

## Endpoint

- **Method:** `POST`
- **Path:** `/partner_api/v1/requests`
- **Base URL:** `https://api.contentsnare.com`
- **Official documentation:** [Create Request](https://api.contentsnare.com/partner_api/v1/documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `client_email` | body | `string` | no | Client email. This will look up an existing client, or create a new one. For a new client, you must also include their full name. |
| `client_full_name` | body | `string` | no | Required for new clients. You may leave blank for existing clients. Providing a value will overwrite the existing name. |
| `client_phone` | body | `string` | no | For existing clients, providing a value will overwrite the existing phone. |
| `comments_enabled` | body | `boolean` | no | Enable client comments. This allows your client to ask questions about each field. |
| `communication_template_id` | body | `string` | no | Id of communications schedule |
| `communication_template_name` | body | `string` | no | Name of communications schedule |
| `company_name` | body | `string` | no | If this company name is not already associated with this client, it will be created. |
| `due` | body | `date` | no | Due date for the request. <br><b>Format:</b> yyyy-mm-dd |
| `folder_id` | body | `string` | no | Folder id. Requests may be grouped in to folders on the requests page. Don't send it if you do not wish to group your Requests. |
| `folder_name` | body | `string` | no | Folder name. Requests may be grouped in to folders on the requests page. Don't send it if you do not wish to group your Requests. |
| `name` | body | `string` | yes | Request name |
| `owner_id` | body | `string` | no | Request owner (team member) id |
| `owner_email` | body | `string` | no | Request owner (team member) email |
| `passcode_enabled` | body | `boolean` | no | Protect share with a pin code. Your client will be asked to set their own pincode when they first access the request. |
| `request_template_id` | body | `string` | no | Request template id (`request_template_id` or `request_template_name` should be set) |
| `request_template_name` | body | `string` | no | Request template name (`request_template_id` or `request_template_name` should be set) |
| `share_via_link_enabled` | body | `boolean` | no | Allow share via link without requiring login |
| `status` | body | `string` | no | Request status |
| `updated_at` | body | `date` | no | Updated At. |
