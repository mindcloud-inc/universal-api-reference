# Add Domain to Blocklist with UserCheck

Adds a domain to the UserCheck blocklist.

## Endpoint

- **Method:** `POST`
- **Path:** `/blocklist`
- **Base URL:** `https://api.usercheck.com`
- **Official documentation:** [Add Domain to Blocklist](https://www.usercheck.com/docs/api/blocklist-endpoint)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | body | `string` | yes | Domain to add to the blocklist. |
