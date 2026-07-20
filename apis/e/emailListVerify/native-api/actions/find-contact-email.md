# Find Contact Email with EmailListVerify

Finds a contact email in EmailListVerify by name or domain.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/findContact`
- **Base URL:** `https://api.emaillistverify.com`
- **Official documentation:** [Find Contact Email](https://api.emaillistverify.com/api-doc#/Verification%20Endpoints/findContact)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | body | `string` | yes | Company email domain to search, such as example.com. |
| `firstName` | body | `string` | no | Optional contact first name. |
| `lastName` | body | `string` | no | Optional contact last name. |
