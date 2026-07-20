# Bulk Add Domains to Blocklist with UserCheck

Adds multiple domains to the UserCheck blocklist.

## Endpoint

- **Method:** `POST`
- **Path:** `/blocklist/bulk`
- **Base URL:** `https://api.usercheck.com`
- **Official documentation:** [Bulk Add Domains to Blocklist](https://www.usercheck.com/docs/api/blocklist-endpoint)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domains[]` | body | `array<string>` | yes | Domains to add to the blocklist. |
