# Create External Share Custom Link with Zoho WorkDrive

Creates an external share link in Zoho WorkDrive.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/links`
- **Base URL:** `{api_domain}/workdrive`
- **Official documentation:** [Create External Share Custom Link](https://workdrive.zoho.com/apidocs/v1/externalsharing/createexternalsharecustomlink)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data.attributes.resource_id` | body | `string` | yes | The file or folder resource ID to share. |
| `data.attributes.link_name` | body | `string` | yes | Display name for the external share link. |
| `data.attributes.request_user_data` | body | `boolean` | yes | Whether the recipient must submit contact information before access. |
| `data.attributes.allow_download` | body | `boolean` | yes | Whether recipients can download the shared resource. |
| `data.attributes.password_text` | body | `string` | no | Optional password that protects the share link. |
| `data.attributes.input_fields` | body | `list` | no | Optional list of custom recipient fields to collect before access. |
| `data.attributes.role_id` | body | `number` | no | Optional role ID that controls the shared permission level. |
| `data.attributes.expiration_date` | body | `string` | no | Optional link expiration date in YYYY-MM-DD format. |
