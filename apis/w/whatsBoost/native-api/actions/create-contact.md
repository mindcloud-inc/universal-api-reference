# Create Contact with WhatsBoost

Creates a new contact in WhatsBoost.

## Endpoint

- **Method:** `POST`
- **Path:** `/create/contact`
- **Base URL:** `https://whatsboost.net/api`
- **Official documentation:** [Create Contact](https://whatsboost.net/api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `phone` | body | `string` | yes | Recipient mobile number, it will accept E.164 formatted number or locally formatted numbers using the country code from your profile settings.  Example for Spain  E.164: +34612345678  Local: 612345678 |
| `name` | body | `string` | yes | Name of contact. |
| `groups` | body | `string` | yes | List of contact group ID's separated by commas. You can get group ID's from /get/groups (Your contact groups). |
