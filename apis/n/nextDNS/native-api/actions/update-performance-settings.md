# Update Performance Settings with NextDNS

Updates performance settings for an existing NextDNS profile.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/profiles/:profile/settings/performance`
- **Base URL:** `https://api.nextdns.io`
- **Official documentation:** [Update Performance Settings](https://nextdns.io/api#nested-objects-and-arrays)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `profile` | path | `string` | yes | NextDNS profile ID. Defaults to the profile ID stored on the connection when available. |
| `ecs` | body | `boolean` | no | Toggle EDNS Client Subnet. |
| `cacheBoost` | body | `boolean` | no | Toggle cache boost. |
| `cnameFlattening` | body | `boolean` | no | Toggle CNAME flattening. |
