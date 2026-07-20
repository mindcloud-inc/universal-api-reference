# Lookup Numbers In Bulk with SMS Connexion

Creates a bulk number lookup in SMS Connexion.

## Endpoint

- **Method:** `POST`
- **Path:** `/numbers/lookup`
- **Base URL:** `https://api.sms.cx`
- **Official documentation:** [Lookup Numbers In Bulk](https://sms.cx/sms-api-documentation/#operation/LookupNumbers)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `phoneNumbers` | body | `object<string>` | yes | E.164 phone numbers to lookup in bulk. |
| `allowInvalid` | body | `boolean` | no | Allow invalid numbers instead of hard validation failure. |
| `countryIso` | body | `string` | no | ISO 3166-1 alpha-2 country used for number validation. |
