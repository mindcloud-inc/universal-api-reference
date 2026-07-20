# List Contact Proceedings with Nimble

Retrieves proceedings for a contact from Nimble.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/contacts/:contact_id/proceedings`
- **Base URL:** `https://app.nimble.com`
- **Official documentation:** [List Contact Proceedings](https://www.nimble.com/developers/docs/#tag/Contacts/operation/list-contact-proceedings)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_id` | path | `string` | yes | Nimble contact_id path parameter. |
| `direction` | query | `string` | yes | — |
| `limit` | query | `number` | yes | — |
