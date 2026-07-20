# Sign Out User by Email with Instant

Signs out an Instant user by email.

## Endpoint

- **Method:** `POST`
- **Path:** `/admin/sign_out`
- **Base URL:** `https://api.instantdb.com`
- **Official documentation:** [Sign Out User by Email](https://www.instantdb.com/docs/http-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | User email address whose sessions should be revoked. |
