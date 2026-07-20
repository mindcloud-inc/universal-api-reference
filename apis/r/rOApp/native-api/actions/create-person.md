# Create Person with RO App

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts/people`
- **Base URL:** `https://api.roapp.io/v2`
- **Official documentation:** [Create Person](https://roapp.readme.io/reference/create-person)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `first_name` | body | `string` | yes | Person first name |
| `last_name` | body | `string` | no | Person last name |
| `birthday` | body | `object` | no | Person birthday |
| `birthday.day` | body | `number` | yes | — |
| `birthday.month` | body | `number` | yes | — |
| `birthday.year` | body | `number` | no | — |
| `email` | body | `string` | no | Valid email |
| `phones[]` | body | `array<object>` | no | List of phone numbers |
| `notes` | body | `string` | no | Notes text |
| `address` | body | `string` | no | Person address |
| `supplier` | body | `boolean` | no | Is this person your supplier? |
| `manager_id` | body | `number` | no | Employee ID |
| `ad_campaign_id` | body | `number` | no | Ad Campaign ID |
| `discount_code` | body | `string` | no | Discount code |
| `custom_fields` | body | `string` | no | Custom fields values in format {"f123": "value", "f234": "value"}, where "f123" and "f234" is a custom field id. |
| `tags[]` | body | `array<string>` | no | Array of tags |
| `tax_identification_number` | body | `string` | no | Tax identification number |
