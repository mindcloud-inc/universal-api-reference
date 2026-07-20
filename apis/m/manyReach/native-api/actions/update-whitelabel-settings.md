# Update Whitelabel Settings with ManyReach

Updates whitelabel settings in ManyReach.

## Endpoint

- **Method:** `PATCH`
- **Path:** `https://api.manyreach.com/api/v2/whitelabel`
- **Base URL:** `https://api.manyreach.com`
- **Official documentation:** [Update Whitelabel Settings](https://api.manyreach.com/api#v2/tag/whitelabel)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `color` | body | `string` | no | Primary whitelabel color. |
| `customDomain` | body | `string` | no | Custom whitelabel domain. |
| `logoImageUrl` | body | `string` | no | Logo image URL for whitelabel branding. |
