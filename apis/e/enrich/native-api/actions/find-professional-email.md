# Find a Professional Email with Enrich.so

Finds a professional email in Enrich.so.

## Endpoint

- **Method:** `POST`
- **Path:** `/email-finder`
- **Base URL:** `https://dev.enrich.so/api/v3`
- **Official documentation:** [Find a Professional Email](https://doc.enrich.so/find-a-professional-email-27483195e0.md)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `firstName` | body | `string` | yes | Person first name. |
| `lastName` | body | `string` | yes | Person last name. |
| `domain` | body | `string` | yes | Company domain. |
