# Add Contact with UpViral

Creates a new contact in UpViral.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://app.upviral.com/api/v1/`
- **Official documentation:** [Add Contact](https://www.upviral.com/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `campaign_id` | body | `string` | yes | The UpViral campaign ID that will receive the contact. |
| `email` | body | `string` | yes | The contact email address. |
| `name` | body | `string` | no | The contact name. |
| `ip_address` | body | `string` | no | The contact IP address. |
| `referral_code` | body | `string` | no | The referrer code from the end of a referral URL. |
| `custom_fields` | body | `object` | no | Custom field values keyed by the campaign's custom field names. |
