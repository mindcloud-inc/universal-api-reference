# Create Environment with SimpleLocalize

Creates a new environment in SimpleLocalize.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/environments`
- **Base URL:** `https://api.simplelocalize.io`
- **Official documentation:** [Create Environment](https://api.simplelocalize.io/openapi/ui#/Hosting/createEnvironment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `key` | body | `string` | yes | Unique key for the environment. Must be lowercase, contain only letters, numbers, and dashes. |
| `name` | body | `string` | yes | Name of the environment. Can contain letters, numbers, spaces, underscores, and dashes. |
| `color` | body | `string` | yes | Color of the environment in hex format for Web UI. Must be 6 characters long and valid hex color. |
