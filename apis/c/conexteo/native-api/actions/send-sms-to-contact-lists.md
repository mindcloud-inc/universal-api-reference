# Send SMS To Contact Lists with Conexteo

Creates an SMS message for Conexteo contact lists.

## Endpoint

- **Method:** `POST`
- **Path:** `/messages/sms/contactlist`
- **Base URL:** `https://api.conexteo.com`
- **Official documentation:** [Send SMS To Contact Lists](https://developers.conexteo.com/envoi-liste-de-contacts-24126510e0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `resumeBefore` | query | `boolean` | no | Return the required credit summary without sending the SMS campaign. Recommended for safe verification. |
| `shorturl` | body | `object` | no | Optional short URL configuration object with mode and url. |
| `external_id` | body | `string` | no | Optional client-provided idempotency key. |
| `scheduleAt` | body | `date` | no | Optional UTC ISO-8601 schedule timestamp. |
| `content` | body | `string` | yes | SMS message body. |
| `sender` | body | `string` | no | Optional sender name, maximum 11 characters. Maximum length: 11. |
| `contactlist[]` | body | `array<string>` | yes | Array of contact-list identifiers. |
