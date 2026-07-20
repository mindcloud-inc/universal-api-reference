# Create Contact with Heyy

Creates a new contact in Heyy.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts`
- **Base URL:** `https://api.heyy.io/api/v2.0/`
- **Official documentation:** [Create Contact](https://docs.heyy.io/api-reference/create-contact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `firstName` | body | `string` | no | The contact first name. |
| `lastName` | body | `string` | no | The contact last name. |
| `phoneNumber` | body | `string` | yes | The contact phone number in E.164 format. |
