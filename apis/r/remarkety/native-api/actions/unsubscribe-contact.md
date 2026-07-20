# Unsubscribe Contact with Remarkety

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/stores/{storeId}/contacts/unsubscribe`
- **Base URL:** `https://app.remarkety.com`
- **Official documentation:** [Unsubscribe Contact](https://support.remarkety.com/hc/en-us/articles/360044121611-Unsubscribing-a-contact-using-API)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `email` | body | `string` | no |
| `sms_phone_number_e164` | body | `string` | no |
| `reason` | body | `string` | no |
