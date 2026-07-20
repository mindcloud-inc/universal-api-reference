# Update Organization with RemOnline

Updates an existing organization in RemOnline.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v2/contacts/organizations/:organization_id`
- **Base URL:** `https://api.roapp.io`
- **Official documentation:** [Update Organization](https://roappua.readme.io/reference/update-organization)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization_id` | path | `number` | yes | ID of the organization. |
| `notes` | body | `string` | no | Notes text. |
| `name` | body | `string` | no | Organization name. |
