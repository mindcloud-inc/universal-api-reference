# Update Tag with SureContact

Updates an existing tag in SureContact.

## Endpoint

- **Method:** `PUT`
- **Path:** `api/v1/public/tags/:tag_uuid`
- **Base URL:** `https://api.surecontact.com`
- **Official documentation:** [Update Tag](https://api.surecontact.com/docs#tag-management-PUTapi-v1-public-tags--tag_uuid-)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `color` | body | `string` | no |
| `description` | body | `string` | no |
| `name` | body | `string` | no |
| `slug` | body | `string` | no |
| `tag_uuid` | path | `string` | yes |
