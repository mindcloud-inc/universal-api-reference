# Tag Devices with Level

Applies a tag to devices in Level.

## Endpoint

- **Method:** `POST`
- **Path:** `/tags/{id}/devices`
- **Base URL:** `https://api.level.io/v2`
- **Official documentation:** [Tag Devices](https://levelapi.readme.io/reference/tagdevices)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `device_ids[]` | body | `array<string>` | yes | An array of device IDs to tag. Send multiple values as a array. |
| `id` | path | `string` | yes | ID of the tag to apply. |
