# Remove Contacts from Tag with SureContact

Removes contacts from an existing SureContact tag.

## Endpoint

- **Method:** `POST`
- **Path:** `api/v1/public/tags/:tag_uuid/contacts/remove`
- **Base URL:** `https://api.surecontact.com`
- **Official documentation:** [Remove Contacts from Tag](https://api.surecontact.com/docs#tag-management-POSTapi-v1-public-tags--tag_uuid--contacts-remove)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `contact_uuids[]` | body | `array<string>` | yes |
| `tag_uuid` | path | `string` | yes |
