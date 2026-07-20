# Update User with Harvestr.io

## Endpoint

- **Method:** `PATCH`
- **Path:** `/user/{id}`
- **Base URL:** `https://rest.harvestr.io/v1`
- **Official documentation:** [Update User](https://developers.harvestr.io/api/update-a-user/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Unique identifier (id or clientId) |
| `name` | body | `string` | no | The name of the user |
| `email` | body | `string` | no | The email address of the user. Set to null to remove |
| `externalUid` | body | `string` | no | External unique identifier for the user from an external system. Set to null to remove |
| `phone` | body | `string` | no | Phone number of the user. Set to null to remove |
| `segments[]` | body | `array<string>` | no | Array of segment names the user belongs to |
| `segments[]` | body | `array<string>` | no | Array of segment names the user belongs to |
| `segments[]` | body | `array<string>` | no | Array of segment names the user belongs to |
| `segments[]` | body | `array<string>` | no | Array of segment names the user belongs to |
| `segments[]` | body | `array<string>` | no | Array of segment names the user belongs to |
| `companyId` | body | `string` | no | ID of the company the user belongs to. Set to null to remove |
