# Reverse Lookup Phone with profileAPI

Finds a person in profileAPI by phone number.

## Endpoint

- **Method:** `POST`
- **Path:** `/phone-contacts/reverse-lookup`
- **Base URL:** `https://api.profileapi.com/2024-03-01`
- **Official documentation:** [Reverse Lookup Phone](https://documentation.profileapi.com/api-reference/reverse-lookup-phone/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `phone` | body | `string` | yes | E.164 phone number to reverse lookup. |
