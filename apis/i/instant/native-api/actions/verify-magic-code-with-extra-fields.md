# Verify Magic Code With Extra Fields with Instant

Verifies a magic code in Instant, setting extra fields on user creation.

## Endpoint

- **Method:** `POST`
- **Path:** `/admin/verify_magic_code`
- **Base URL:** `https://api.instantdb.com`
- **Official documentation:** [Verify Magic Code With Extra Fields](https://www.instantdb.com/docs/http-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | User email address tied to the magic code. |
| `code` | body | `string` | yes | Magic code to verify. |
| `extra-fields` | body | `object` | no | Optional custom $users fields to set when creating the user. |
