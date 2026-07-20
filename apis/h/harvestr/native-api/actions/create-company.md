# Create Company with Harvestr.io

## Endpoint

- **Method:** `POST`
- **Path:** `/company`
- **Base URL:** `https://rest.harvestr.io/v1`
- **Official documentation:** [Create Company](https://developers.harvestr.io/api/create-a-company/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The name of the company |
| `externalUid` | body | `string` | no | External unique identifier for the company from an external system |
| `segments[]` | body | `array<string>` | no | Array of segment names the company belongs to |
| `segments[]` | body | `array<string>` | no | Array of segment names the company belongs to |
