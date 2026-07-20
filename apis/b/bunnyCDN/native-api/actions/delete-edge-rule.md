# Delete Edge Rule with BunnyCDN

Deletes an edge rule from a BunnyCDN pull zone.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/pullzone/:pullZoneId/edgerules/:edgeRuleId`
- **Base URL:** `https://api.bunny.net`
- **Official documentation:** [Delete Edge Rule](https://docs.bunny.net/reference/bunnynet-api-overview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `edgeRuleId` | path | `string` | yes | The Bunny edge rule ID. |
| `pullZoneId` | path | `string` | yes | The Bunny pull zone ID. |
