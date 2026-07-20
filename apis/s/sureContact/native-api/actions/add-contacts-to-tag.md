# Add Contacts to Tag with SureContact

Adds contacts to an existing SureContact tag.

## Endpoint

- **Method:** `POST`
- **Path:** `api/v1/public/tags/:tag_uuid/contacts/add`
- **Base URL:** `https://api.surecontact.com`
- **Official documentation:** [Add Contacts to Tag](https://api.surecontact.com/docs#tag-management-POSTapi-v1-public-tags--tag_uuid--contacts-add)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `contact_uuids[]` | body | `array<string>` | yes |
| `tag_uuid` | path | `string` | yes |
