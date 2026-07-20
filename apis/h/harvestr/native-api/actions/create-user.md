# Create User with Harvestr.io

## Endpoint

- **Method:** `POST`
- **Path:** `/user`
- **Base URL:** `https://rest.harvestr.io/v1`
- **Official documentation:** [Create User](https://developers.harvestr.io/api/create-a-user/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The name of the user |
| `email` | body | `string` | no | The email address of the user |
| `externalUid` | body | `string` | no | External unique identifier for the user from an external system |
| `phone` | body | `string` | no | Phone number of the user |
| `segments[]` | body | `array<string>` | no | Array of segment names the user belongs to |
| `segments[]` | body | `array<string>` | no | Array of segment names the user belongs to |
| `segments[]` | body | `array<string>` | no | Array of segment names the user belongs to |
| `segments[]` | body | `array<string>` | no | Array of segment names the user belongs to |
| `segments[]` | body | `array<string>` | no | Array of segment names the user belongs to |
| `companyId` | body | `string` | no | ID of the company the user belongs to |
