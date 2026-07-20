# Lookup Phone with profileAPI

Finds a phone contact in profileAPI by person details.

## Endpoint

- **Method:** `POST`
- **Path:** `/phone-contacts/lookup`
- **Base URL:** `https://api.profileapi.com/2024-03-01`
- **Official documentation:** [Lookup Phone](https://documentation.profileapi.com/api-reference/lookup-phone/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | no | Person UUID option for phone lookup. |
| `firstName` | body | `string` | no | First-name field for name plus website phone lookup. |
| `lastName` | body | `string` | no | Last-name field for name plus website phone lookup. |
| `website` | body | `string` | no | Company website for name plus website phone lookup. |
| `linkedInUrl` | body | `string` | no | LinkedIn profile URL lookup option. |
