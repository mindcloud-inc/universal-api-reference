# Update Company with Harvestr.io

## Endpoint

- **Method:** `PATCH`
- **Path:** `/company/{id}`
- **Base URL:** `https://rest.harvestr.io/v1`
- **Official documentation:** [Update Company](https://developers.harvestr.io/api/update-a-company/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Unique identifier (id or clientId) |
| `name` | body | `string` | no | The name of the company |
| `externalUid` | body | `string` | no | External unique identifier for the company from an external system. Set to null to remove |
| `segments[]` | body | `array<string>` | no | Array of segment names the company belongs to |
| `segments[]` | body | `array<string>` | no | Array of segment names the company belongs to |
