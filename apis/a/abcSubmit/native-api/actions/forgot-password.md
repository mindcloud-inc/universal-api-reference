# Forgot Password with AbcSubmit

Requests an AbcSubmit password reset email.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/users/forgot-password`
- **Base URL:** `https://www.abcsubmit.com`
- **Official documentation:** [Forgot Password](https://www.abcsubmit.com/site/api-documentation/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | The email address associated with the AbcSubmit account. |
