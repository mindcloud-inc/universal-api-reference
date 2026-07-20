# Check Feature Gates with Statsig

Checks feature gates in Statsig.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/check_gate`
- **Base URL:** `https://statsigapi.net`
- **API:** rest
- **Official documentation:** [Check Feature Gates](https://docs.statsig.com/api-reference/feature-gates/check-feature-gates)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `gateName` | body | `string` | yes | Single gate name to check. Use this or gateNames. |
| `gateNames` | body | `list<string>` | no | Array of gate names to check. Use this or gateName. |
| `user` | body | `object` | yes | Statsig user object containing at least one identifier. |
| `statsigMetadata` | body | `object` | no | SDK metadata for diagnostics and exposure behavior. |
