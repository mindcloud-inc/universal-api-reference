# Create Response with Missive

Creates a response in your Missive workspace.

## Endpoint

- **Method:** `POST`
- **Path:** `/responses`
- **Base URL:** `https://public.missiveapp.com/v1`
- **Official documentation:** [Create Response](https://missiveapp.com/docs/developers/rest-api/endpoints#create-response-s)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `attachments[].base64_data` | body | `string` | no | Base64-encoded attachment content |
| `attachments[].filename` | body | `string` | no | Attachment filename string |
| `attachments[].id` | body | `string` | no | Existing upload ID string |
| `bcc_fields[].address` | body | `string` | no | BCC recipient email address string |
| `bcc_fields[].name` | body | `string` | no | BCC recipient display name string |
| `body` | body | `string` | no | HTML string containing the response content |
| `cc_fields[].address` | body | `string` | no | CC recipient email address string |
| `cc_fields[].name` | body | `string` | no | CC recipient display name string |
| `external_id` | body | `string` | no | External provider ID string |
| `external_source` | body | `string` | no | External provider source string |
| `organization` | body | `string` | no | Organization ID string. Either organization or user is required, but not both. |
| `share_with_team` | body | `string` | no | Team ID string |
| `shared_labels[]` | body | `string` | no | Array of organization label ID strings |
| `subject` | body | `string` | no | Response subject string |
| `title` | body | `string` | no | Response title string (max 500 characters) |
| `to_fields[].address` | body | `string` | no | Recipient email address string |
| `to_fields[].name` | body | `string` | no | Recipient display name string |
| `user` | body | `string` | no | User ID string for personal responses. Either organization or user is required, but not both. |
