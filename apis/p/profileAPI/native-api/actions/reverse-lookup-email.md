# Reverse Lookup Email with profileAPI

Finds a person in profileAPI by email address.

## Endpoint

- **Method:** `POST`
- **Path:** `/email-contacts/reverse-lookup`
- **Base URL:** `https://api.profileapi.com/2024-03-01`
- **Official documentation:** [Reverse Lookup Email](https://documentation.profileapi.com/api-reference/reverse-lookup-email/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | Email address to reverse lookup. |
