# Run Bulk DNS Lookup with Botster

Creates a Botster bulk DNS lookup job.

## Endpoint

- **Method:** `POST`
- **Path:** `/bots/bulk-dns-lookup`
- **Base URL:** `https://botster.io/api/v2`
- **Official documentation:** [Run Bulk DNS Lookup](https://botster.io/bots/bulk-dns-lookup)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input` | body | `string` | yes | Domain names. |
| `skip` | body | `string` | no | Comma-separated DNS record types to skip. |
