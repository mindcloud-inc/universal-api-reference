# Create Contact Tag with Constant Contact

Creates a contact tag in Constant Contact.

## Endpoint

- **Method:** `POST`
- **Path:** `/contact_tags`
- **Base URL:** `https://api.cc.email/v3`
- **Official documentation:** [Create Contact Tag](https://developer.constantcontact.com/api_guide/tags_create.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Name of the tag to create. |
| `tag_source` | body | `string` | no | Tag source type when provided by the API. |
