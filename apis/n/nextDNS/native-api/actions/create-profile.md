# Create Profile with NextDNS

Creates a new configuration profile in NextDNS.

## Endpoint

- **Method:** `POST`
- **Path:** `/profiles`
- **Base URL:** `https://api.nextdns.io`
- **Official documentation:** [Create Profile](https://nextdns.io/api#profile)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Profile name. |
| `security` | body | `object` | no | Profile security settings object. |
| `privacy` | body | `object` | no | Profile privacy settings object. |
| `parentalControl` | body | `object` | no | Profile parental control settings object. |
| `denylist[]` | body | `array<object>` | no | Profile denylist array. |
| `allowlist[]` | body | `array<object>` | no | Profile allowlist array. |
| `settings` | body | `object` | no | Profile settings object. |
