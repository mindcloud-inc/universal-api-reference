# Generate SSO Login Link with Shuffler

Creates an SSO login link in Shuffler.

## Endpoint

- **Method:** `POST`
- **Path:** `/orgs/sso/link`
- **Base URL:** `https://shuffler.io/api/v1`
- **Official documentation:** [Generate SSO Login Link](https://shuffler.io/docs/API#generate-sso-login-link)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | User email. |
