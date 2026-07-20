# Update Group with Innform

Updates an existing group in Innform.

## Endpoint

- **Method:** `PUT`
- **Path:** `/groups/{id}`
- **Base URL:** `https://api.innform.io/v1`
- **Official documentation:** [Update Group](https://innform.docs.apiary.io/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `color` | body | `string` | no | Updated hex color value. |
| `id` | path | `string` | yes | Group UUID. |
| `name` | body | `string` | no | Updated group name. |
