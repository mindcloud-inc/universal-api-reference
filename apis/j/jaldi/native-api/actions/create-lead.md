# Create Lead with Jaldi

Creates a new lead in Jaldi.

## Endpoint

- **Method:** `POST`
- **Path:** `/add_on/webhook/add`
- **Base URL:** `https://api.jalditech.com`
- **Official documentation:** [Create Lead](https://jalditech.com/support/sending-leads-to-jaldi-via-webhooks-connect-to-website-lead-forms/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `camp_id` | body | `string` | yes | The Jaldi campaign_id that should receive the new lead. |
| `lead_f_name` | body | `string` | yes | Lead first name. |
| `lead_phone` | body | `string` | yes | Lead phone number in Jaldi's recommended +CountryCode format. |
| `lead_l_name` | body | `string` | no | Lead last name. |
| `lead_email` | body | `string` | no | Lead email address. |
| `lead_uploaded_notes` | body | `string` | no | Optional notes sent with the lead. |
