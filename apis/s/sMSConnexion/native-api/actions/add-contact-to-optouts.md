# Add Contact To Optouts with SMS Connexion

Adds contacts to the optout list in SMS Connexion.

## Endpoint

- **Method:** `POST`
- **Path:** `/optouts`
- **Base URL:** `https://api.sms.cx`
- **Official documentation:** [Add Contact To Optouts](https://sms.cx/sms-api-documentation/#operation/AddContactToOptoutsList)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `phoneNumbers` | body | `object<string>` | yes | E.164 phone numbers to add to the optout list. |
| `allowInvalid` | body | `boolean` | no | Allow invalid numbers instead of hard validation failure. |
| `countryIso` | body | `string` | no | ISO 3166-1 alpha-2 country used for number validation. |
