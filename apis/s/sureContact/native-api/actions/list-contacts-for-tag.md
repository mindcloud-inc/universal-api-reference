# List Contacts for Tag with SureContact

Retrieves contacts assigned to a SureContact tag.

## Endpoint

- **Method:** `GET`
- **Path:** `api/v1/public/tags/:tag_uuid/contacts`
- **Base URL:** `https://api.surecontact.com`
- **Official documentation:** [List Contacts for Tag](https://api.surecontact.com/docs#tag-management-GETapi-v1-public-tags--tag_uuid--contacts)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `per_page` | query | `number` | no |
| `tag_uuid` | path | `string` | yes |
