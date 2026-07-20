# Create Contact Group with EZ Texting

Creates a contact group in EZ Texting.

## Endpoint

- **Method:** `POST`
- **Path:** `/contact-groups`
- **Base URL:** `https://a.eztexting.com/v1`
- **Official documentation:** [Create Contact Group](https://developers.eztexting.com/reference/create_1-1)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `groupIds[]` | body | `array<string>` | no | Nested contact groups to include |
| `name` | body | `string` | yes | Contact group name |
| `note` | body | `string` | no | Contact group note |
| `phoneNumbers[]` | body | `array<string>` | no | Phone numbers to include in the group |
| `strictValidation` | body | `boolean` | no | Require strict validation for provided contacts |
