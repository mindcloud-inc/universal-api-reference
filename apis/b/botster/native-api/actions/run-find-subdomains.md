# Run Find Subdomains with Botster

Creates a Botster subdomain discovery job.

## Endpoint

- **Method:** `POST`
- **Path:** `/bots/find-subdomains`
- **Base URL:** `https://botster.io/api/v2`
- **Official documentation:** [Run Find Subdomains](https://botster.io/bots/find-subdomains)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `input` | body | `string` | yes | Domain to inspect for known subdomains. |
