# Collect User Consent for Guidance Services with Bridge

Collects user consent for guidance services in Bridge.

## Endpoint

- **Method:** `POST`
- **Path:** `/guidance/consents`
- **Base URL:** `https://api.bridgeapi.io/v3`
- **Official documentation:** [Collect User Consent for Guidance Services](https://docs.bridgeapi.io/reference/createguidanceconsent)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user_uuid` | body | `string` | yes | The UUID of the user giving consent |
| `country_code` | body | `string` | no | The ISO 3166-1 alpha-2 country code (2 letters) |
| `company_identification_number` | body | `string` | yes | The identification number of the company (SIREN, ...) (9 digits) |
| `contact_email` | body | `string` | no | Optional contact email address |
| `contact_phone_number` | body | `string` | no | Optional contact phone number |
