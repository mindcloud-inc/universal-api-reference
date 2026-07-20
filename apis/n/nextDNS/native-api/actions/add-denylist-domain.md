# Add Denylist Domain with NextDNS

Creates a denylist domain entry in a NextDNS profile.

## Endpoint

- **Method:** `POST`
- **Path:** `/profiles/:profile/denylist`
- **Base URL:** `https://api.nextdns.io`
- **Official documentation:** [Add Denylist Domain](https://nextdns.io/api#nested-objects-and-arrays)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `profile` | path | `string` | yes | NextDNS profile ID. Defaults to the profile ID stored on the connection when available. |
| `id` | body | `string` | yes | Domain to add to the denylist. |
| `active` | body | `boolean` | no | Whether the denylist entry is active. |
