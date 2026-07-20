# Update Buyer with Digistore24

Updates an existing buyer in Digistore24.

## Endpoint

- **Method:** `PUT`
- **Path:** `/updateBuyer`
- **Base URL:** `https://www.digistore24.com/api/call`
- **Official documentation:** [Update Buyer](https://digistore24.com/api/docs/paths/updateBuyer.yaml)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `buyer_id` | query | `number` | yes | Buyer ID |
| `email` | body | `string` | no | Buyer email address |
| `first_name` | body | `string` | no | Buyer first name |
| `last_name` | body | `string` | no | Buyer last name |
| `salutation` | body | `string` | no | Buyer salutation |
| `title` | body | `string` | no | Buyer title |
| `company` | body | `string` | no | Buyer company |
| `street_name` | body | `string` | no | Street name |
| `street_number` | body | `string` | no | Street number |
| `phone_number` | body | `string` | no | Phone number |
| `city` | body | `string` | no | City |
| `zipcode` | body | `string` | no | ZIP or postal code |
| `state` | body | `string` | no | State or province |
| `country` | body | `string` | no | ISO country code |
