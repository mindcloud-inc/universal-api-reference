# Validate User Credentials with Cerbo

Validates Cerbo user login credentials.

## Endpoint

- **Method:** `POST`
- **Path:** `/users/validate_credentials`
- **Base URL:** `https://{tenant}.md-hq.com/api/v1`
- **Official documentation:** [Validate User Credentials](https://docs.cer.bo/#tag/Users/operation/validateUserCredentials)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `user` | body | `string` | yes | username |
| `password` | body | `string` | yes | — |
