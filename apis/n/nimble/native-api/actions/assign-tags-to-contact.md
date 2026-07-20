# Assign Tags to Contact with Nimble

Updates tags for a contact in Nimble.

## Endpoint

- **Method:** `PUT`
- **Path:** `/api/v1/contacts/:contact_id/tags`
- **Base URL:** `https://app.nimble.com`
- **Official documentation:** [Assign Tags to Contact](https://www.nimble.com/developers/docs/#tag/Contacts/operation/put-contact-tags)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contact_id` | path | `string` | yes | Nimble contact_id path parameter. |
| `tags[]` | body | `array<string>` | yes | — |
