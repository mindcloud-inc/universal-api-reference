# Create Organization with RO App

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts/organizations`
- **Base URL:** `https://api.roapp.io/v2`
- **Official documentation:** [Create Organization](https://roapp.readme.io/reference/create-organization)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Organization name |
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
