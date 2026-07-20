# Remove Domain from Blocklist with UserCheck

Removes a domain from the UserCheck blocklist.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/blocklist/:domain`
- **Base URL:** `https://api.usercheck.com`
- **Official documentation:** [Remove Domain from Blocklist](https://www.usercheck.com/docs/api/blocklist-endpoint)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `domain` | path | `string` | yes | Domain to remove from the blocklist. |
