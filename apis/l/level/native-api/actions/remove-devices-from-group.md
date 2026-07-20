# Remove Devices from Group with Level

Removes devices from a group in Level.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/groups/{id}/devices`
- **Base URL:** `https://api.level.io/v2`
- **Official documentation:** [Remove Devices from Group](https://levelapi.readme.io/reference/removegroupdevices)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `device_ids[]` | body | `array<string>` | yes | An array of device IDs to remove from the group. Send multiple values as a array. |
| `id` | path | `string` | yes | ID of the group. |
