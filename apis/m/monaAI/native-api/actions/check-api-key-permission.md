# Check API Key Permission with Mona AI

Checks whether a Mona AI API key has a specific permission.

## Endpoint

- **Method:** `POST`
- **Path:** `/auth/checkIfAPIKeyHasPermission`
- **Base URL:** `https://api.mona-ai.cloud`
- **Official documentation:** [Check API Key Permission](https://api-docs.mona-ai.cloud/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `permission` | body | `string` | yes | Mona permission string to check, as documented in the request body. |
