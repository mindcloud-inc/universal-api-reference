# Update Contact Status with SureContact

Updates a contact's status in SureContact.

## Endpoint

- **Method:** `PATCH`
- **Path:** `api/v1/public/contacts/:contact_uuid/status`
- **Base URL:** `https://api.surecontact.com`
- **Official documentation:** [Update Contact Status](https://api.surecontact.com/docs#contact-management-PATCHapi-v1-public-contacts--contact_uuid--status)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_uuid` | path | `string` | yes | The UUID of the contact. |
| `status` | body | `string` | yes | The new status for the contact. |
