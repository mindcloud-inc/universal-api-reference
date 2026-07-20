# Upsert Contact with Remarkety

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/stores/{storeId}/contacts`
- **Base URL:** `https://app.remarkety.com`
- **Official documentation:** [Upsert Contact](https://support.remarkety.com/hc/en-us/articles/115000520263-Sending-contact-information-via-API)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `email` | body | `string` | no |
| `sms_phone_number` | body | `string` | no |
| `sms_country_code` | body | `string` | no |
| `firstName` | body | `string` | no |
| `lastName` | body | `string` | no |
| `tags[]` | body | `array<string>` | no |
| `marketingAllowed` | body | `boolean` | no |
| `smsMarketingAllowed` | body | `boolean` | no |
| `doubleOptin` | body | `boolean` | no |
