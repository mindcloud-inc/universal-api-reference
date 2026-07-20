# Lookup Contact By Phone Number with Aloware

Finds a contact in Aloware by phone number.

## Endpoint

- **Method:** `GET`
- **Path:** `/api/v1/webhook/contact/phone-number`
- **Base URL:** `https://app.aloware.com`
- **Official documentation:** [Lookup Contact By Phone Number](https://support.aloware.com/en/articles/9020068-aloware-contact-lookup-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `phone_number` | query | `string` | yes | Phone number of the contact you want to look up. |
