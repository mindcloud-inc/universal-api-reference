# Create Organization with RemOnline

Creates a new organization in RemOnline.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/contacts/organizations`
- **Base URL:** `https://api.roapp.io`
- **Official documentation:** [Create Organization](https://roappua.readme.io/reference/create-organization)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Organization name. |
| `email` | body | `string` | no | Organization email address. |
| `phones[]` | body | `array<object>` | no | Array of phone objects. Send multiple values as a array. |
| `notes` | body | `string` | no | Notes text. |
| `address` | body | `string` | no | Organization address. |
| `supplier` | body | `boolean` | no | Whether the organization is a supplier. |
| `manager_id` | body | `number` | no | Manager ID. |
| `ad_campaign_id` | body | `number` | no | Advertising campaign ID. |
| `discount_code` | body | `string` | no | Discount code. |
| `custom_fields` | body | `object` | no | Custom fields object. |
| `tags[]` | body | `array<string>` | no | Array of tags. Send multiple values as a array. |
| `tax_identification_number` | body | `string` | no | Tax identification number. |
| `business_registration_number` | body | `string` | no | Business registration number. |
