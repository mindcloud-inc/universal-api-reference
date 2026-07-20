# Update Device Group with Viewneo

Updates an existing device group in Viewneo.

## Endpoint

- **Method:** `POST`
- **Path:** `/devicegroup/:id`
- **Base URL:** `https://cloud.viewneo.com/api/v1.0`
- **Official documentation:** [Update Device Group](https://cloud.viewneo.com/doc/api#/DeviceGroup/api.deviceGroup.update)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `id` | path | `number` | yes |
| `name` | body | `string` | no |
| `display_app_properties` | body | `number` | yes |
| `is_notification_enabled` | body | `number` | yes |
