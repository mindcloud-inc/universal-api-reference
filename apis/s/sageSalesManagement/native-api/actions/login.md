# Login with Sage Sales Management

Retrieves a session key from Sage Sales Management.

## Endpoint

- **Method:** `POST`
- **Path:** `/login`
- **Base URL:** `https://api.forcemanager.com/api/v4`
- **Official documentation:** [Login](https://developer.forcemanager.com/)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `username` | body | `string` | yes | Public API key sent to the login endpoint as the username. |
| `password` | body | `string` | yes | Private API key sent to the login endpoint as the password. |
