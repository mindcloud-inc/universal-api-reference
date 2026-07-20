# Add Or Update Edge Rule with BunnyCDN

Adds or updates an edge rule in BunnyCDN.

## Endpoint

- **Method:** `POST`
- **Path:** `/pullzone/:pullZoneId/edgerules/addOrUpdate`
- **Base URL:** `https://api.bunny.net`
- **Official documentation:** [Add Or Update Edge Rule](https://docs.bunny.net/reference/bunnynet-api-overview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `pullZoneId` | path | `string` | yes | The Bunny pull zone ID. |
| `ActionType` | body | `string` | yes | Edge rule action type enum value. |
