# Verify Email with Kickbox

Verifies an email address with Kickbox.

## Endpoint

- **Method:** `GET`
- **Path:** `/verify`
- **Base URL:** `https://api.kickbox.com/v2`
- **Official documentation:** [Verify Email](https://docs.kickbox.com/docs/single-verification-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | query | `string` | yes | The email address to verify, URL-encoded. |
| `timeout` | query | `number` | no | Maximum time in milliseconds for the verification request. Default 6000, maximum 30000. |
