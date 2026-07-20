# Delete Contact with SureContact

Deletes an existing contact from SureContact.

## Endpoint

- **Method:** `DELETE`
- **Path:** `api/v1/public/contacts/:contact_uuid`
- **Base URL:** `https://api.surecontact.com`
- **Official documentation:** [Delete Contact](https://api.surecontact.com/docs#contact-management-DELETEapi-v1-public-contacts--contact_uuid-)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_uuid` | path | `string` | yes | The UUID of the contact. |
