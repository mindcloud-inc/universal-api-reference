# Validate Authentication Token with Softr

## Endpoint

- **Method:** `POST`
- **Path:** `https://priscilla41205.softr.app/v1/api/users/validate-token`
- **Base URL:** `https://tables-api.softr.io/api/v1`
- **Official documentation:** [Validate Authentication Token](https://docs.softr.io/softr-api/api-setup-and-endpoints#validate-an-authentication-token)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `jwt` | body | `string` | yes | JWT token for the Softr user session to validate. |
