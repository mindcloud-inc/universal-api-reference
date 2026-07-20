# Create Device with Tiliter

Creates a device in the Tiliter Recognition API.

## Endpoint

- **Method:** `POST`
- **Path:** `/devices/:device_id`
- **Base URL:** `https://recognition.services.tiliter.com/v1/15`
- **Official documentation:** [Create Device](https://developer.tiliter.com/reference/create_device)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `device_id` | path | `string` | yes | — |
| `deviceId` | body | `string` | yes | Device ID in the request body. Must match Device ID Path. |
| `cameras[]` | body | `array<string>` | yes | — |
| `cameras[]` | body | `array<string>` | yes | — |
| `operationalMode` | body | `string` | yes | — |
| `storeId` | body | `string` | yes | — |
| `departments[]` | body | `array<string>` | yes | — |
| `departments[]` | body | `array<string>` | yes | — |
