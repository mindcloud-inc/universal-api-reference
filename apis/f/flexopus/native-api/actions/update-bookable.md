# Update Bookable with Flexopus

Updates an existing bookable in Flexopus.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/bookables/:id`
- **Base URL:** `{tenantBaseUrl}/api/v1`
- **Official documentation:** [Update Bookable](https://flexopus.com/api/docs/#endpoints-PATCHapi-v1-bookables--id-)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | ID of the bookable object to update. |
| `name` | body | `string` | no | Name of the object. |
| `description` | body | `string` | no | Description of the object. Set null to clear it. |
| `status` | body | `list<number>` | no | Desired status of the object. Accepted values: `0`, `1`. |
| `tags[]` | body | `array<string>` | no | Full list of tags to set on the object. |
