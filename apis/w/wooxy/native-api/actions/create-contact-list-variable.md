# Create Contact List Variable with Wooxy

Creates a new contact list variable in Wooxy.

## Endpoint

- **Method:** `POST`
- **Path:** `v3/contact-list/variables/add`
- **Base URL:** `https://api.wooxy.com`
- **Official documentation:** [Create Contact List Variable](https://wooxy.com/api-documentation/contact-list/add-contact-list-variable)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactListId` | body | `string` | yes | Wooxy contact list ID. |
| `variables[]` | body | `array<object>` | yes | Array of variable objects with required name and type (ENUM_STRING or ENUM_DATE). |
