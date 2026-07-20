# Create Account Tag with Fliqr AI

Creates a new account tag in Fliqr AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/accounts/tags`
- **Base URL:** `https://app.fliqr.ai/api/`
- **Official documentation:** [Create Account Tag](https://docs.fliqr.ai/api-reference/accounts/post-accountstags)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/x-www-form-urlencoded` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Tag name. |
