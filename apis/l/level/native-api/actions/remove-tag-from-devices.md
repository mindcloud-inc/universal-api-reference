# Remove Tag from Devices with Level

Removes a tag from devices in Level.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/tags/{id}/devices`
- **Base URL:** `https://api.level.io/v2`
- **Official documentation:** [Remove Tag from Devices](https://levelapi.readme.io/reference/removetagfromdevices)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `device_ids[]` | body | `array<string>` | yes | An array of device IDs to remove the tag from. Send multiple values as a array. |
| `id` | path | `string` | yes | ID of the tag to remove. |
