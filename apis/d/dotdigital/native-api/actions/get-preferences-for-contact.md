# Get Preferences for Contact with Dotdigital

Retrieves a contact's preference opt-ins from Dotdigital.

## Endpoint

- **Method:** `GET`
- **Path:** `/v2/contacts/:contactIdentifier/preferences`
- **Base URL:** `https://r2-api.dotmailer.com`
- **Official documentation:** [Get Preferences for Contact](https://developer.dotdigital.com/reference/get-preferences-for-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `contactIdentifier` | path | `string` | yes | Use either the contact ID or the contact email address. |
