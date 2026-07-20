# Verify Magic Code with Instant

Verifies a magic code in Instant.

## Endpoint

- **Method:** `POST`
- **Path:** `/admin/verify_magic_code`
- **Base URL:** `https://api.instantdb.com`
- **Official documentation:** [Verify Magic Code](https://www.instantdb.com/docs/http-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | User email address tied to the magic code. |
| `code` | body | `string` | yes | Magic code to verify. |
