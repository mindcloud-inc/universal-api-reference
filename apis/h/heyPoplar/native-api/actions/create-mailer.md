# Create Mailer with HeyPoplar

Creates a new mailer in HeyPoplar.

## Endpoint

- **Method:** `POST`
- **Path:** `/mailing`
- **Base URL:** `https://api.heypoplar.com/v1`
- **Official documentation:** [Create Mailer](https://docs.heypoplar.com/api/endpoints/mailing#create-mailer)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign_id` | body | `string` | yes | ID of the campaign to use for the mailing. |
| `creative_id` | body | `string` | no | Optional creative ID. If omitted, Poplar uses the default creative. |
| `send_at` | body | `string` | no | Future ISO8601 timestamp for when the mailing should be sent. |
| `recipient.full_name` | body | `string` | no | Optional recipient name. Poplar uses Current Resident if omitted. |
| `recipient.email` | body | `string` | no | Optional recipient email address. |
| `recipient.address_1` | body | `string` | yes | Recipient street address. |
| `recipient.city` | body | `string` | yes | Recipient city. |
| `recipient.state` | body | `string` | yes | Recipient state abbreviation. |
| `recipient.postal_code` | body | `string` | yes | Recipient postal code. |
