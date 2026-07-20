# Remove Contact Attribute with Heyy

Removes an attribute from a contact in Heyy.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/contacts/:contactId/attributes`
- **Base URL:** `https://api.heyy.io/api/v2.0/`
- **Official documentation:** [Remove Contact Attribute](https://docs.heyy.io/api-reference/remove-contact-attribute)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactId` | path | `string` | yes | The Heyy contact ID. |
| `externalId` | body | `string` | yes | The contact attribute external ID to remove. |
