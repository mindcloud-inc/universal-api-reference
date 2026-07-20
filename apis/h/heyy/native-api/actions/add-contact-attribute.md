# Add Contact Attribute with Heyy

Adds an attribute to a contact in Heyy.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts/:contactId/attributes`
- **Base URL:** `https://api.heyy.io/api/v2.0/`
- **Official documentation:** [Add Contact Attribute](https://docs.heyy.io/api-reference/add-contact-attribute)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactId` | path | `string` | yes | The Heyy contact ID. |
| `externalId` | body | `string` | yes | The contact attribute external ID. |
| `value` | body | `string` | yes | The attribute value. |
