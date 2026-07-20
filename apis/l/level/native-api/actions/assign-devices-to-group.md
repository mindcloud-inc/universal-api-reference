# Assign Devices to Group with Level

Assigns devices to a group in Level.

## Endpoint

- **Method:** `POST`
- **Path:** `/groups/{id}/devices`
- **Base URL:** `https://api.level.io/v2`
- **Official documentation:** [Assign Devices to Group](https://levelapi.readme.io/reference/assigndevicestogroup)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `device_ids[]` | body | `array<string>` | yes | An array of device IDs to assign to the group. Send multiple values as a array. |
| `id` | path | `string` | yes | ID of the group. |
