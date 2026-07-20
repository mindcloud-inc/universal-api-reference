# Update Organization with Zammad

Updates an existing organization in Zammad.

## Endpoint

- **Method:** `PUT`
- **Path:** `/organizations/:id`
- **Base URL:** `{baseUrl}/api/v1`
- **Official documentation:** [Update Organization](https://docs.zammad.org/en/latest/api/organization.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Organization ID. |
| `note` | body | `string` | yes | Organization note. |
