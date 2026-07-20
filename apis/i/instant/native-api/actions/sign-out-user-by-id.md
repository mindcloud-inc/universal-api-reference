# Sign Out User by ID with Instant

Signs out an Instant user by ID.

## Endpoint

- **Method:** `POST`
- **Path:** `/admin/sign_out`
- **Base URL:** `https://api.instantdb.com`
- **Official documentation:** [Sign Out User by ID](https://www.instantdb.com/docs/http-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | body | `string` | yes | Instant user ID whose sessions should be revoked. |
