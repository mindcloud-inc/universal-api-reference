# Attach File To Entity with Fibery

Attaches a file to an entity in Fibery.

## Endpoint

- **Method:** `POST`
- **Path:** `/commands`
- **Base URL:** `https://{account}.fibery.io/api`
- **Official documentation:** [Attach File To Entity](https://the.fibery.io/@public/User_Guide/Guide/File-API-265)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `type` | body | `string` | yes |
| `field` | body | `string` | yes |
| `entity` | body | `object` | yes |
| `items[]` | body | `array<object>` | yes |
