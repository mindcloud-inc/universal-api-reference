# Set Edge Rule Enabled with BunnyCDN

Updates an edge rule's enabled status in BunnyCDN.

## Endpoint

- **Method:** `POST`
- **Path:** `/pullzone/:pullZoneId/edgerules/:edgeRuleId/setEdgeRuleEnabled`
- **Base URL:** `https://api.bunny.net`
- **Official documentation:** [Set Edge Rule Enabled](https://docs.bunny.net/reference/bunnynet-api-overview)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `edgeRuleId` | path | `string` | yes | The Bunny edge rule ID. |
| `pullZoneId` | path | `string` | yes | The Bunny pull zone ID. |
| `Value` | body | `string` | yes | Whether the edge rule should be enabled. |
