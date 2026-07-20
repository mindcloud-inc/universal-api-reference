# Run Bulk Whois Lookup with Botster

Creates a Botster bulk WHOIS lookup job.

## Endpoint

- **Method:** `POST`
- **Path:** `/bots/bulk-whois-lookup`
- **Base URL:** `https://botster.io/api/v2`
- **Official documentation:** [Run Bulk Whois Lookup](https://botster.io/bots/bulk-whois-lookup)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input` | body | `string` | yes | Domain names. |
