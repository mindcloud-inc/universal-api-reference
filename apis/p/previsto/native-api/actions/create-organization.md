# Create Organization with Previsto

Creates a new organization in Previsto.

## Endpoint

- **Method:** `POST`
- **Path:** `/organizations`
- **Base URL:** `https://api.previsto.io`
- **Official documentation:** [Create Organization](https://developer.previsto.com/organization/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address` | body | `string` | no | Street address |
| `city` | body | `string` | no | City |
| `countryCode` | body | `string` | no | 2-letter country code |
| `location` | body | `string` | yes | Location as [longitude, latitude]. Required by the live API. |
| `name` | body | `string` | yes | Organization name. |
| `postalCode` | body | `string` | no | Postal code |
| `languageCode` | body | `string` | yes | Organization language code. |
| `baseCurrency` | body | `string` | no | Organization base currency. |
| `timeZone` | body | `string` | no | Organization time zone. |
