# Add Custom Hostname with BunnyCDN

Adds a custom hostname to a BunnyCDN pull zone.

## Endpoint

- **Method:** `POST`
- **Path:** `/pullzone/:id/addHostname`
- **Base URL:** `https://api.bunny.net`
- **Official documentation:** [Add Custom Hostname](https://docs.bunny.net/reference/bunnynet-api-overview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Bunny pull zone ID. |
| `Hostname` | body | `string` | yes | Hostname to add to the pull zone. |
