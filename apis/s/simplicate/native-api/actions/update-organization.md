# Update Organization with Simplicate

## Endpoint

- **Method:** `PUT`
- **Path:** `/crm/organization/:id`
- **Base URL:** `https://{subdomain}/api/v2`
- **Official documentation:** [Update Organization](https://developer.simplicate.com/docs/api/v2/reference/update-crm-organization/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | no | Organization id path parameter from the Simplicate update organization endpoint. |
| `name` | body | `string` | no | Organization name from the Simplicate update organization request body. |
| `note` | body | `string` | no | Optional organization note from the Simplicate update organization request body. |
