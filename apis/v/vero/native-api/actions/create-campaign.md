# Create Campaign with Vero

Creates a new campaign in Vero.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v4/campaigns`
- **Base URL:** `https://api.getvero.com`
- **Official documentation:** [Create Campaign](https://help.getvero.com/api-reference/campaigns/create-a-campaign)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `audience` | body | `string` | no | Optional audience reference. |
| `id` | body | `string` | yes | The campaign identifier. Must match Vero's campaign_* pattern. |
| `status` | body | `string` | no | Optional campaign status. |
| `object` | body | `string` | yes | The resource type. Vero documents this as campaign. |
| `title` | body | `string` | yes | The internal campaign title. |
| `action` | body | `object` | yes | The campaign action object. |
| `trigger` | body | `object` | no | Optional trigger reference or expanded trigger object. |
| `conversion` | body | `object` | no | Optional conversion object. |
| `archived` | body | `boolean` | no | Optional archived flag. |
