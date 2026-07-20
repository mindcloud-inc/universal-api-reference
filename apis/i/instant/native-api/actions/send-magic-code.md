# Send Magic Code with Instant

Sends a magic code with Instant email.

## Endpoint

- **Method:** `POST`
- **Path:** `/admin/send_magic_code`
- **Base URL:** `https://api.instantdb.com`
- **Official documentation:** [Send Magic Code](https://www.instantdb.com/docs/http-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `email` | body | `string` | yes | User email address to send a magic code to. |
