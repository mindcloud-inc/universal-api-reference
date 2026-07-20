# Save space with Platrum

Creates or updates a knowledge space in Platrum.

## Endpoint

- **Method:** `POST`
- **Path:** `/wiki/api/space/save`
- **Base URL:** `https://3e8e7be.platrum.com`
- **Official documentation:** [Save space](http://api.docs.platrum.ru/modules/wiki/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `access_edit[]` | body | `array<object>` | no | Edit access rules. |
| `access_rules[]` | body | `array<object>` | no | Permission rules. |
| `access[]` | body | `array<object>` | no | View access rules. |
| `description` | body | `string` | no | Space description. |
| `id` | body | `number` | no | Space ID for updates. |
| `is_archived` | body | `boolean` | no | Whether the space is archived. |
| `is_public` | body | `boolean` | no | Whether the space is public. |
| `slug` | body | `string` | no | Space slug. |
| `title` | body | `string` | no | Space title. |
