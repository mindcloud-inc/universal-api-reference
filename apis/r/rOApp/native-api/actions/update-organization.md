# Update Organization with RO App

## Endpoint

- **Method:** `PATCH`
- **Path:** `/contacts/organizations/:organization_id`
- **Base URL:** `https://api.roapp.io/v2`
- **Official documentation:** [Update Organization](https://roapp.readme.io/reference/update-organization)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organization_id` | path | `number` | yes | Organization ID |
| `name` | body | `string` | no | Organization name |
| `email` | body | `string` | no | Organization email |
| `phones[]` | body | `array<object>` | no | List of phone numbers |
| `notes` | body | `string` | no | Notes text |
| `address` | body | `string` | no | Organization address |
| `supplier` | body | `boolean` | no | Is this organization your supplier? |
| `manager_id` | body | `number` | no | Employee ID |
| `ad_campaign_id` | body | `number` | no | Ad Campaign ID |
| `discount_code` | body | `string` | no | Discount code |
| `custom_fields` | body | `string` | no | Custom fields values in format {"f123": "value", "f234": "value"}, where "f123" and "f234" is a custom field id. |
| `tags[]` | body | `array<string>` | no | Array of tags |
| `tax_identification_number` | body | `string` | no | Tax identification number |
| `business_registration_number` | body | `string` | no | Business registration number |
