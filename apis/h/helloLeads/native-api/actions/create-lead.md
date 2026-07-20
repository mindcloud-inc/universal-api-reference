# Create Lead with HelloLeads

## Endpoint

- **Method:** `POST`
- **Path:** `leads`
- **Base URL:** `https://app.helloleads.io/index.php/private/api`
- **Official documentation:** [Create Lead](https://app.helloleads.io/index.php/app/account/layout#/apisettings)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address_line1` | body | `string` | no | First line of the lead address. |
| `address_line2` | body | `string` | no | Second line of the lead address. |
| `category` | body | `string` | no | Lead category. |
| `city` | body | `string` | no | Lead city. |
| `company` | body | `string` | no | Company or organization name. |
| `country` | body | `string` | no | Lead country. |
| `deal_size` | body | `string` | no | Lead deal size as accepted by HelloLeads. |
| `designation` | body | `string` | no | Lead designation or job title. |
| `fax` | body | `string` | no | Lead fax number. |
| `first_name` | body | `string` | yes | Lead first name. HelloLeads requires this field for lead creation. |
| `interests` | body | `string` | no | Lead interests. |
| `mobile_code` | body | `string` | no | Mobile country code prefix, for example +1. |
| `notes` | body | `string` | no | Lead notes. |
| `phone` | body | `string` | no | Lead phone number. |
| `postal_code` | body | `string` | no | Lead postal or ZIP code. |
| `potential` | body | `string` | no | Lead potential value, for example Low, Medium, or High. |
| `state` | body | `string` | no | Lead state or region. |
| `tags` | body | `string` | no | Comma-separated or provider-native tag value. |
| `website` | body | `string` | no | Lead website URL. |
| `list_key` | body | `list` | yes | HelloLeads list identifier for the destination list. Live verification used the Website Enquires list. |
| `email` | body | `string` | no | Lead email address. |
| `mobile` | body | `string` | no | Lead mobile number. |
| `last_name` | body | `string` | no | Lead last name. |
