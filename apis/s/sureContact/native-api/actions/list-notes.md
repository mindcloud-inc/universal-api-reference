# List Notes with SureContact

Retrieves notes for a SureContact contact.

## Endpoint

- **Method:** `GET`
- **Path:** `api/v1/public/contacts/:contact_uuid/notes`
- **Base URL:** `https://api.surecontact.com`
- **Official documentation:** [List Notes](https://api.surecontact.com/docs#contact-notes-GETapi-v1-public-contacts--contact_uuid--notes)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_uuid` | path | `string` | yes | The UUID of the contact. |
| `page` | query | `number` | no | Page number. |
| `per_page` | query | `number` | no | Number of items per page. |
