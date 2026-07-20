# Create List with SendMails

Creates a new list in SendMails.

## Endpoint

- **Method:** `POST`
- **Path:** `/lists`
- **Base URL:** `https://app.sendmails.io/api/v1`
- **Official documentation:** [Create List](https://sendmails.io/docs/campaigns-apis-by-sendmails-io/#3-toc-title)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | query | `string` | yes | List name. |
| `from_email` | query | `string` | yes | Default from email address. |
| `from_name` | query | `string` | yes | Default from name. |
| `contact[company]` | query | `string` | yes | Company name. |
| `contact[state]` | query | `string` | yes | State, province, or region. |
| `contact[address_1]` | query | `string` | yes | Address line 1. |
| `contact[address_2]` | query | `string` | yes | Address line 2. |
| `contact[city]` | query | `string` | yes | City. |
| `contact[zip]` | query | `string` | yes | Zip or postal code. |
| `contact[phone]` | query | `string` | yes | Phone number. |
| `contact[country_id]` | query | `string` | yes | Country ID. |
| `contact[email]` | query | `string` | yes | Contact email address. |
| `contact[url]` | query | `string` | no | Optional home page URL. |
| `subscribe_confirmation` | query | `string` | no | Send subscription confirmation email. |
| `send_welcome_email` | query | `string` | no | Send a welcome email. |
| `unsubscribe_notification` | query | `string` | no | Send unsubscribe notification to subscribers. |
