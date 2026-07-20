# Create Account with Recurly

## Endpoint

- **Method:** `POST`
- **Path:** `/accounts`
- **Base URL:** `https://v3.recurly.com`
- **Official documentation:** [Create Account](https://recurly.com/developers/api/v2021-02-25/#operation/create_account)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `code` | body | `string` | yes | Unique account code. |
| `company` | body | `string` | no | Company name. |
| `email` | body | `string` | no | Account email address. |
| `first_name` | body | `string` | no | Billing first name. |
| `last_name` | body | `string` | no | Billing last name. |
| `preferred_locale` | body | `string` | no | Locale code for hosted experiences and emails. |
| `preferred_time_zone` | body | `string` | no | Time zone identifier for the account. |
| `tax_exempt` | body | `boolean` | no | Whether the account is tax exempt. |
| `username` | body | `string` | no | Optional account username. |
