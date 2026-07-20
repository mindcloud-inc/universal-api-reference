# Search Phone Numbers with Bolna

Finds available phone numbers by region, locality, or pattern.

## Endpoint

- **Method:** `GET`
- **Path:** `/phone-numbers/search`
- **Base URL:** `https://api.bolna.ai`
- **Official documentation:** [Search Phone Numbers](https://www.bolna.ai/docs/api-reference/phone-numbers/search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `country` | query | `string` | yes | Country code for the phone-number search, such as US or IN. |
| `pattern` | query | `string` | no | Three-character prefix to search against the phone number. |
| `provider` | query | `string` | no | Telephony provider filter for the search result. |
