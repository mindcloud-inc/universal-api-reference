# Create Driver with Samsara

## Endpoint

- **Method:** `POST`
- **Path:** `fleet/drivers`
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
| `driverActivationStatus` | body | `string` | no |
