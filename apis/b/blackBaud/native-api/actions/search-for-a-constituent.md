# Search For A Constituent with BlackBaud

## Endpoint

- **Method:** `GET`
- **Path:** `alt-conmg/constituents/search`
- **Base URL:** `https://api.sky.blackbaud.com/`
- **Official documentation:** [Search For A Constituent](https://learn.microsoft.com/en-us/connectors/blackbaudaltruconsti/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `key_name` | query | `string` | no | Last name for individuals or organization name for organizations. |
| `first_name` | query | `string` | no | The constituent first name. |
| `lookup_id` | query | `string` | no | The constituent lookup ID. |
| `email_address` | query | `string` | no | The constituent email address. |
| `phone_number` | query | `string` | no | The constituent phone number. |
| `exact_match_only` | query | `boolean` | no | Match all criteria exactly. |
| `include_individuals` | query | `boolean` | no | Include individual constituents. |
| `include_organizations` | query | `boolean` | no | Include organization constituents. |
| `include_deceased` | query | `boolean` | no | Include deceased constituents. |
