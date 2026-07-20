# Lookup Email with profileAPI

Finds an email contact in profileAPI by person details.

## Endpoint

- **Method:** `POST`
- **Path:** `/email-contacts/lookup`
- **Base URL:** `https://api.profileapi.com/2024-03-01`
- **Official documentation:** [Lookup Email](https://documentation.profileapi.com/api-reference/lookup-email/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | no | Person UUID option for email lookup. |
| `firstName` | body | `string` | no | First-name field for name plus website email lookup. |
| `lastName` | body | `string` | no | Last-name field for name plus website email lookup. |
| `website` | body | `string` | no | Company website for name plus website email lookup. |
| `linkedInUrl` | body | `string` | no | LinkedIn profile URL lookup option. |
| `type` | body | `list` | no | Email type to return: professional or personal. Accepted values: `0`, `1`. |
