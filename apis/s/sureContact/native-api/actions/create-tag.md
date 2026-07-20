# Create Tag with SureContact

Creates a new tag in SureContact.

## Endpoint

- **Method:** `POST`
- **Path:** `api/v1/public/tags`
- **Base URL:** `https://api.surecontact.com`
- **Official documentation:** [Create Tag](https://api.surecontact.com/docs#tag-management-POSTapi-v1-public-tags)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `color` | body | `string` | no |
| `description` | body | `string` | no |
| `name` | body | `string` | yes |
| `slug` | body | `string` | no |
