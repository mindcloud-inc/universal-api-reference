# Create Person with RemOnline

Creates a new person in RemOnline.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/contacts/people`
- **Base URL:** `https://api.roapp.io`
- **Official documentation:** [Create Person](https://roappua.readme.io/reference/create-person)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `first_name` | body | `string` | yes | Person first name. |
| `last_name` | body | `string` | no | Person last name. |
| `birthday` | body | `object` | no | Birthday object. |
| `email` | body | `string` | no | Valid email address. |
| `phones[]` | body | `array<object>` | no | Array of phone objects. Send multiple values as a array. |
| `notes` | body | `string` | no | Notes text. |
| `address` | body | `string` | no | Person address. |
| `supplier` | body | `boolean` | no | Whether the person is a supplier. |
| `manager_id` | body | `number` | no | Manager ID. |
| `ad_campaign_id` | body | `number` | no | Advertising campaign ID. |
| `discount_code` | body | `string` | no | Discount code. |
| `custom_fields` | body | `object` | no | Custom fields object. |
| `tags[]` | body | `array<string>` | no | Array of tags. Send multiple values as a array. |
| `tax_identification_number` | body | `string` | no | Tax identification number. |
