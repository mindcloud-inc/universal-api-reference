# Update Settings with Camio

Updates settings in Camio.

## Endpoint

- **Method:** `POST`
- **Path:** `/users/:user/settings`
- **Base URL:** `https://camio.com/api`
- **Official documentation:** [Update Settings](https://api.camio.com/#update-settings)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `recording_enabled` | body | `boolean` | no | Enable or disable account-wide recording. |
