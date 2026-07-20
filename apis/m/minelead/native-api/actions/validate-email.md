# Validate Email with Minelead

Validates an email address with Minelead.

## Endpoint

- **Method:** `GET`
- **Path:** `/validate`
- **Base URL:** `https://api.minelead.io/v1`
- **Official documentation:** [Validate Email](https://api.minelead.io/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | yes | Email address to validate. |
| `firstname` | query | `string` | no | First name associated with the email. |
| `lastname` | query | `string` | no | Last name associated with the email. |
