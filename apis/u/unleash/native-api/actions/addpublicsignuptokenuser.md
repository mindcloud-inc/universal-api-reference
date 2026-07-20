# Add A User Via A Signup Token with Unleash

Adds a user via a signup token in Unleash.

## Endpoint

- **Method:** `POST`
- **Path:** `/invite/{token}/signup`
- **Base URL:** `https://us.app.getunleash.io/uspp0456`
- **Official documentation:** [Add A User Via A Signup Token](https://docs.getunleash.io/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `object` | yes | Required JSON request body. |
| `token` | path | `string` | yes | Required path parameter. |
