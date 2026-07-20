# Retrieve Blocklist Scan Status with Postmaster+

Retrieves blocklist scan status from Postmaster+.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/blocklist/scan/status/:id`
- **Base URL:** `https://postmasterplus.app`
- **Official documentation:** [Retrieve Blocklist Scan Status](https://postmasterplus.app/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The ULID of the blocklist check. |
