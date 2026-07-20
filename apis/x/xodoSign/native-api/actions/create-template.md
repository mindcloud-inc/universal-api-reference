# Create Template with Xodo Sign

Creates a new template in Xodo Sign.

## Endpoint

- **Method:** `POST`
- **Path:** `/document`
- **Base URL:** `https://api.eversign.com`
- **Official documentation:** [Create Template](https://eversign.com/api/documentation/methods#create-template)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `business_id` | query | `string` | yes | The Xodo Sign business ID that owns the new template. |
| `is_draft` | body | `string` | no | Set to 1 to save the template as a draft. |
| `sandbox` | body | `string` | no | Set to 1 to enable sandbox mode for template creation. |
| `title` | body | `string` | no | Title for the template. |
