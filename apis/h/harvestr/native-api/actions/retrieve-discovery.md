# Retrieve Discovery with Harvestr.io

## Endpoint

- **Method:** `GET`
- **Path:** `/discovery/{id}`
- **Base URL:** `https://rest.harvestr.io/v1`
- **Official documentation:** [Retrieve Discovery](https://developers.harvestr.io/api/retrieve-a-discovery/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | Unique identifier (id or clientId) |
| `select` | query | `string` | no | Comma-separated list of additional relations to include in response. Available: 'discoveryfields' |
