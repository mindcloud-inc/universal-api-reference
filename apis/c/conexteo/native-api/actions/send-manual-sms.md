# Send Manual SMS with Conexteo

Creates a manual SMS message in Conexteo.

## Endpoint

- **Method:** `POST`
- **Path:** `/messages/sms`
- **Base URL:** `https://api.conexteo.com`
- **Official documentation:** [Send Manual SMS](https://developers.conexteo.com/envoi-manuel-24126508e0)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `resumeBefore` | query | `boolean` | no | Return the required credit summary without sending the SMS campaign. Recommended for safe verification. |
| `shorturl` | body | `object` | no | Optional short URL configuration object with mode and url. |
| `external_id` | body | `string` | no | Optional client-provided idempotency key. |
| `scheduleAt` | body | `date` | no | Optional UTC ISO-8601 schedule timestamp. |
| `content` | body | `string` | yes | SMS message body. |
| `sender` | body | `string` | no | Optional sender name, maximum 11 characters. Maximum length: 11. |
| `recipients[]` | body | `array<string>` | yes | Array of recipient phone numbers in national or E.164 format. |
