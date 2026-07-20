# Create Squid with LOBSTR.IO

Creates a new squid in LOBSTR.IO.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/squids`
- **Base URL:** `https://api.lobstr.io`
- **Official documentation:** [Create Squid](https://docs.lobstr.io/docs/create-squid)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `crawler` | body | `string` | yes | The unique ID (hash) of the crawler to use for this squid. |
| `name` | body | `string` | no | Custom name for the squid. |
