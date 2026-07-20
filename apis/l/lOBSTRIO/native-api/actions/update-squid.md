# Update Squid with LOBSTR.IO

Updates an existing squid in LOBSTR.IO.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/squids/:squid_hash`
- **Base URL:** `https://api.lobstr.io`
- **Official documentation:** [Update Squid](https://docs.lobstr.io/docs/update-squid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `is_active` | body | `boolean` | no | Enable (true) or disable (false) the squid. |
| `name` | body | `string` | no | Display name for the squid. |
| `squid_hash` | path | `string` | yes | The unique identifier (hash) of the squid. |
