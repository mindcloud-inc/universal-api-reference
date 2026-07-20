# Find Phone Numbers with Enrich.so

Finds phone numbers in Enrich.so by email or profile URL.

## Endpoint

- **Method:** `GET`
- **Path:** `/reverse-lookup/phones`
- **Base URL:** `https://dev.enrich.so/api/v3`
- **Official documentation:** [Find Phone Numbers](https://doc.enrich.so/find-phone-numbers-27483199e0.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | no | Email address to use for phone lookup. Provide this or LinkedIn. |
| `linkedin` | query | `string` | no | LinkedIn/profile URL to use for phone lookup. Provide this or Email. |
