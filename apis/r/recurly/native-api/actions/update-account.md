# Update Account with Recurly

## Endpoint

- **Method:** `PUT`
- **Path:** `/accounts/:account_id`
- **Base URL:** `https://v3.recurly.com`
- **Official documentation:** [Update Account](https://recurly.com/developers/api/v2021-02-25/#operation/update_account)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `account_id` | path | `string` | yes | Recurly account ID or code. |
| `bill_to` | body | `string` | no | Billing responsibility setting for hierarchical accounts. |
| `company` | body | `string` | no | Updated company name. |
| `email` | body | `string` | no | Updated account email address. |
| `first_name` | body | `string` | no | Updated billing first name. |
| `last_name` | body | `string` | no | Updated billing last name. |
| `preferred_locale` | body | `string` | no | Updated preferred locale. |
| `preferred_time_zone` | body | `string` | no | Updated preferred time zone. |
| `tax_exempt` | body | `boolean` | no | Whether the account is tax exempt. |
