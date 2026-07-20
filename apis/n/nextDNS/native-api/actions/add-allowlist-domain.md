# Add Allowlist Domain with NextDNS

Creates an allowlist domain entry in a NextDNS profile.

## Endpoint

- **Method:** `POST`
- **Path:** `/profiles/:profile/allowlist`
- **Base URL:** `https://api.nextdns.io`
- **Official documentation:** [Add Allowlist Domain](https://nextdns.io/api#nested-objects-and-arrays)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `profile` | path | `string` | yes | NextDNS profile ID. Defaults to the profile ID stored on the connection when available. |
| `id` | body | `string` | yes | Domain to add to the allowlist. |
| `active` | body | `boolean` | no | Whether the allowlist entry is active. |
