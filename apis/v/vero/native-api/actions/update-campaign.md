# Update Campaign with Vero

Updates an existing campaign in Vero.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/api/v4/campaigns/:id`
- **Base URL:** `https://api.getvero.com`
- **Official documentation:** [Update Campaign](https://help.getvero.com/api-reference/campaigns/update-a-campaign)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `audience` | body | `string` | no | Optional audience reference update. |
| `id` | path | `string` | yes | The campaign identifier. |
| `status` | body | `string` | no | Optional campaign status update. |
| `title` | body | `string` | no | Optional campaign title update. |
| `action` | body | `object` | no | Optional campaign action object update. |
| `trigger` | body | `object` | no | Optional trigger reference or expanded trigger object update. |
| `conversion` | body | `object` | no | Optional conversion object update. |
| `archived` | body | `boolean` | no | Optional archived flag update. |
