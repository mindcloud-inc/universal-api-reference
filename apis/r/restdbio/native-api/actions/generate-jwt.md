# Generate JWT with Restdb.io

Generates a JWT token in Restdb.io.

## Endpoint

- **Method:** `POST`
- **Path:** `/auth/jwt`
- **Base URL:** `https://mindcloudstage0-7934.restdb.io`
- **Official documentation:** [Generate JWT](https://restdb.io/media/restdb-cheat-sheet.pdf)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `payload` | body | `string` | yes | JSON object with JWT claims. |
| `secret` | body | `string` | yes | Path to the JWT secret configured in Restdb.io global settings. |
