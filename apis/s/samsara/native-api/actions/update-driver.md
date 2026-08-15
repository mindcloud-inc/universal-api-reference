# Update Driver with Samsara

## Endpoint

- **Method:** `PATCH`
- **Path:** `fleet/drivers/:driverId`
- **Base URL:** `https://api.samsara.com/`

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `externalIds` | body | `object<object>` | no |
| `name` | body | `string<object>` | no |
| `password` | body | `string<object>` | no |
| `tagIds[]` | body | `array<string>` | no |
| `username` | body | `string<string>` | no |
| `driverId` | path | `string` | no |
| `driverActivationStatus` | body | `string` | no |
| `deactivatedAtTime` | body | `string` | no |
