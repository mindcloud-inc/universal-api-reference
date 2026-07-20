# Create a User API Key with Xata

## Endpoint

- **Method:** `POST`
- **Path:** `/api-keys`
- **Base URL:** `https://api.xata.tech`
- **Official documentation:** [Create a User API Key](https://xata.io/docs/api-reference/api-keys/create-a-user-api-key)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | — |
| `expiry` | body | `string` | no | Expiration date for the API key, null for no expiry |
| `scopes[]` | body | `array` | no | Optional scopes assigned to the API key |
| `scopes[]` | body | `array` | no | Optional scopes assigned to the API key |
| `projects[]` | body | `array` | no | Limit access to these projects |
| `projects[]` | body | `array` | no | Limit access to these projects |
| `branches[]` | body | `array` | no | Limit access to these branches |
| `branches[]` | body | `array` | no | Limit access to these branches |
